# forecast_solar custom integration

The integration add´s to the "power production now" sensor attributes with the forecast list.

## Installation
Copy the folder to your custom_integration folder in Home Assistant
The Integration replaces the main Forecast Solar integration and uses the allready configured sensor. 
the Power Production Now sensor will expand with attributes.

## Configuration of the Template Sensor
To combine every single forcast solar sensor you need to add the template sensor example to your configuration.
You have to adapt the template sesnor for your need´s.

## Configuration with spilted config file

>[!NOTE]
>Information how to split your home assitant configuration:
>https://www.home-assistant.io/docs/configuration/splitting_configuration/
>
Copy forecast_solar_sensor.yaml to the `/config/packes`

Add following to your configuration:
```
homeassistant:
  packages: !include_dir_named packages
```
## Configuration of evcc
https://github.com/evcc-io/evcc/issues/18857#issuecomment-2664731520
