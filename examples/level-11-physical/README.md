# Level 11: Physical-Digital Bridge

## The Shift

The IDE becomes a control surface for reality.

```
AI Agent → Home Assistant REST API → Device
                                        ↓
                                  Sensor feedback
                                        ↓
                            Home Assistant → Agent context
```

## Agent Controls Office Environment

```javascript
const HA_URL = process.env.HA_URL;
const HA_TOKEN = process.env.HA_TOKEN;

async function callService(domain, service, entityId, data = {}) {
  return fetch(`${HA_URL}/api/services/${domain}/${service}`, {
    method: 'POST',
    headers: { 'Authorization': `Bearer ${HA_TOKEN}`, 'Content-Type': 'application/json' },
    body: JSON.stringify({ entity_id: entityId, ...data }),
  }).then(r => r.json());
}

async function prepareOfficeForCall() {
  const temp = await fetch(`${HA_URL}/api/states/sensor.office_temperature`,
    { headers: { 'Authorization': `Bearer ${HA_TOKEN}` } }).then(r => r.json());

  if (parseFloat(temp.state) > 24)
    await callService('climate', 'set_temperature', 'climate.office_ac', { temperature: 22 });

  await callService('light', 'turn_on', 'light.office_desk', { brightness: 200, color_temp: 350 });
  await callService('light', 'turn_off', 'light.office_overhead');
}
```

## 3D Print Orchestration via OctoPrint

```javascript
const OCTO_URL = process.env.OCTOPRINT_URL;
const OCTO_KEY = process.env.OCTOPRINT_KEY;

async function startPrint(filename) {
  await fetch(`${OCTO_URL}/api/files/local/${filename}`, {
    method: 'POST',
    headers: { 'X-Api-Key': OCTO_KEY, 'Content-Type': 'application/json' },
    body: JSON.stringify({ command: 'select', print: true }),
  });
}

async function emergencyStop() {
  await fetch(`${OCTO_URL}/api/job`, {
    method: 'POST',
    headers: { 'X-Api-Key': OCTO_KEY, 'Content-Type': 'application/json' },
    body: JSON.stringify({ command: 'cancel' }),
  });
  console.log('EMERGENCY STOP');
}
```

## Physical Safety Backpressure

```javascript
const SAFETY_LIMITS = {
  maxTemperature: 28,
  minTemperature: 16,
  maxPowerDraw: 3000,
  maxPrintDuration: 480,  // minutes
  maxFilamentCost: 50,    // USD
};

// The human override: a PHYSICAL kill switch that cannot be software-bypassed
// Hardware button or smart plug that cuts power
// Not a software toggle — software can be wrong, hardware can't lie
```

## Level Up Checklist

- [ ] Agent reads at least one physical sensor
- [ ] Agent controls at least one physical device
- [ ] Physical safety limits block unsafe actions
- [ ] Physical kill switch exists (not software)
- [ ] Agent actions produced a real-world change
- [ ] Feedback loop: agent acts → sensor confirms → agent adjusts
