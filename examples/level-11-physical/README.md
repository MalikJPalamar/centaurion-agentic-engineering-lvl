# Level 11: Physical-Digital Bridge

## The Shift
Your agent does not just write code. It controls physical devices, reads sensors, and triggers manufacturing.

## Home Assistant as the Bridge Layer
```
AI Agent -> Home Assistant REST API -> Device (lights, HVAC, printer)
                                            |
                                      Sensor feedback
                                            |
                              Home Assistant -> Agent context
```

## Example: Agent Controls Office Environment

```javascript
const HA_URL = process.env.HA_URL;
const HA_TOKEN = process.env.HA_TOKEN;

async function callService(domain, service, entityId, data = {}) {
  const response = await fetch(`${HA_URL}/api/services/${domain}/${service}`, {
    method: 'POST',
    headers: {
      'Authorization': `Bearer ${HA_TOKEN}`,
      'Content-Type': 'application/json',
    },
    body: JSON.stringify({ entity_id: entityId, ...data }),
  });
  return response.json();
}

async function getSensorState(entityId) {
  const response = await fetch(`${HA_URL}/api/states/${entityId}`, {
    headers: { 'Authorization': `Bearer ${HA_TOKEN}` },
  });
  return response.json();
}

async function prepareOfficeForCall() {
  const temp = await getSensorState('sensor.office_temperature');
  const co2 = await getSensorState('sensor.office_co2');
  const actions = [];
  if (parseFloat(temp.state) > 24) {
    actions.push(callService('climate', 'set_temperature',
      'climate.office_ac', { temperature: 22 }));
  }
  if (parseInt(co2.state) > 1000) {
    actions.push(callService('fan', 'turn_on',
      'fan.office_purifier', { percentage: 75 }));
  }
  actions.push(callService('light', 'turn_on',
    'light.office_desk', { brightness: 200, color_temp: 350 }));
  await Promise.all(actions);
}
```

## Physical Safety Backpressure
This is what makes Level 11 fundamentally different. A bug in code wastes tokens. A bug in a physical control loop wastes material, energy, or worse.

### Required Safety Constraints
```javascript
const SAFETY_LIMITS = {
  maxTemperature: 28,      // degrees C
  minTemperature: 16,
  maxPowerDraw: 3000,      // Watts
  maxPrintDuration: 480,   // minutes
  maxFilamentCost: 50,     // USD
};

// The human override: a PHYSICAL kill switch
// Not a software toggle. Hardware that cuts power.
// Software can be wrong. Hardware cannot lie.
```

## Level Up Checklist
- [ ] Agent reads at least one physical sensor
- [ ] Agent controls at least one physical device
- [ ] Physical safety limits block agent actions outside safe ranges
- [ ] You have a physical kill switch (not software) for critical devices
- [ ] Agent actions have produced a real-world change you can see or touch
