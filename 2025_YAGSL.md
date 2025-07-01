# How to put YAGSL on your robot!
This is documentation for setting up YAGSL for swerve drive.

---
## Walkthrough

1. Fork the [repository](https://github.com/Chicago-Robotics-Alliance/2025_CRA_Commons)
2. Make sure that the owner of the fork is your team's organization.
3. Clone this forked repository and open it in 2025 WPILib VS Code.
4. Build the code: If you are in CPS you will probably not be able to access any of the referenced libraries in github.io so you might have to build at home. If you get errors trying to build the code that is probably because CPS is blocking github.io (look at errors and see if that is the case). Using a personal device and non-cps wifi at school would work.
5. Edit .wpilib\wpilib_preferences.json, specifically the year and your team number.
6. For all the next steps use [yagsl documentation](https://docs.yagsl.com/) as reference.
7. Find the folder ```~/src/main/deploy/swerve/robot```
8. Configure the JSON files. You can use [this website](https://broncbotz3481.github.io/YAGSL-Example/) to help.

```swervedrive.json``` -
- change the ```"type"``` based on your IMU (NavX, Pigeon, etc.).
- you need to know the id and change the ```"id"``` accordingly.
- change the ```"invertedIMU"``` to ```true``` if the gyro is inverted.

```/modules``` -
- change the IDs of drive based on your motor IDs
- change the type based on your motor type [using the bottom of this page](https://docs.yagsl.com/devices/motor-controllers)
- follow this [documentation](https://docs.yagsl.com/configuring-yagsl/configuration/swerve-module-configuration) to get more information for each feature in the config jsons, refer to your past swerve code to find the values, and your manufacturer of your model.

```physicalproperties.json``` - 
- find the drive and steer gear ratios: find them from your swerve drive manufacturer.
- the diameter is the wheel diameter in inches (by default that is 4, which might be correct already).
- The gear ratios are probably the hardest to find.
