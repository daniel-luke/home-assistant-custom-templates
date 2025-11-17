## Custom IR Fan control in Home Assistant

### Setup
1. Create an input boolean helper. (In the example, it is called: input_boolean.bedroom_fan_state)
2. Create an input number helper. (In the example, it is called: input_number.bedroom_fan_percentage)
3. Record the following IR commands:
- Go to the development tools
- select `Actions`
- Select the `remote.lean_command` action
- In the device input, give it a name (In the example, it is called: ceiling_fans, as I use the same set of learnt commands to control multiple fans)
- For the command name, use these commands:
  - off: When the off button has been pressed
  - low: When the low speed button has been pressed
  - medium: When the medium speed button has been pressed
  - high: When the high speed button has been pressed
5. Copy the contents of `device.yaml` into your configuration
6. Copy the contents of `scripts.yaml` into your configuration
7. Change the naming if needed to be more suitable to your use case.
- Keep in mind that you need to change the device_id in all the scripts!
