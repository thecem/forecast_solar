# forecast_solar custom integration

The integration add´s to the "power production now" sensor attributes with the forecast list.

## Installation
Copy `/forecast_solar` to your `/custom_integration`  in Home Assistant
The Integration replaces the main Forecast Solar integration and uses the allready configured sensor. 
the Power Production Now sensor will expand with attributes.
>[!NOTE]
>Your home assitant configuration will be not attached!
>If you would like to revert, delete the folder or set in file manifest.json version to 0.0.1, this switchs after a reboot the custom integration off.
>
```
{
    ...,
    "requirements": ["forecast-solar==4.0.0"],
    "version": "0.0.1"  // 0.0.0 -> Use Custom integration / 0.0.1 -> Don´t use 
}
```


## Configuration
### Template Sensor
To combine every single forcast solar sensor you need to add the template sensor example to your configuration.
You have to adapt the template sesnor for your need´s.

### Spilted config file

>[!NOTE]
>Information how to split your home assitant configuration:
>https://www.home-assistant.io/docs/configuration/splitting_configuration/
>
Copy forecast_solar_sensor.yaml to `/config/packages`

Add following to your configuration:
```
homeassistant:
  packages: !include_dir_named packages
```
### evcc
https://github.com/evcc-io/evcc/issues/18857#issuecomment-2664731520
