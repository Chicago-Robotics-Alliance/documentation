# How to put YAGSL on your robot!
This is documentation for setting up YAGSL for swerve drive.

---
## Walkthrough

1. Fork the repository
2. Make sure that the owner of the fork is your team's organization.
3. Clone this forked repository and open it in WPILib VS Code.
4. Find the folder ```~/src/main/deploy/swerve/(some file name that holds all the java files)```
5. Edit the swervedrive.json -
~~~
{
  "imu": {
    "type": "navx",
    "id": 0,
    "canbus": null
  },
  "invertedIMU": false,
  "modules": [
    "frontleft.json",
    "frontright.json",
    "backleft.json",
    "backright.json"
  ]
}
~~~
- change the ```"type"``` based on your gyro.
- change the ```"invertedIMU"``` to ```true``` if the gyro is inverted.
6. Edit the swerve modules json files in ```/modules``` -
~~~
{
  "drive": {
    "type": "talonfx",
    "id": 23,
    "canbus": null
  },
  "angle": {
    "type": "talonfx",
    "id": 22,
    "canbus": null
  },
  "encoder": {
    "type": "cancoder",
    "id": 61,
    "canbus": null
  },
  "inverted": {
    "drive": false,
    "angle": false
  },
  "absoluteEncoderOffset": 75.7,
  "location": {
    "front": -13,
    "left": 11.375
  }
}
~~~
- change the IDs of drive based on your motor IDs
- change the type based on your motor type [using the bottom of this page](https://docs.yagsl.com/devices/motor-controllers)
- follow this [documentation](https://docs.yagsl.com/configuring-yagsl/configuration/swerve-module-configuration) to get more information for each feature in the config jsons, refer to your past swerve code to find the values, and your manufacturer.
