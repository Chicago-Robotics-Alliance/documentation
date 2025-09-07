# How to code real-time PID tuning
This is documentation for using Shuffleboard to change PID values in real-time for any mechanism

---
## Walkthrough - Mechanisms
1. Open the file for the subsystem you are trying to do this for. Refer to the example Climber subsystem in the [2025_Commons repo](https://github.com/Chicago-Robotics-Alliance/2025_CRA_Commons/blob/main/src/main/java/frc/robot/subsystems/Climber.java)
2. Set up the PID controller - use the link above for an example implementation.
3. import shuffleboard using `import edu.wpi.first.wpilibj.smartdashboard.SmartDashboard;`
4. in the periodic method (`public void periodic() {}`) enter the line `SmartDashboard.putData("title of the card", the PID data);` For example: `SmartDashboard.putData("ClimberPID", climberPID);` This line of code will automatically send your PID values to the shuffleboard which can be changed and stored.
5. once you have found the right PID values, change the pre-meditated values with your tuned values. Feel free to comment the shuffleboard code.
---
## Serve
Have a look at the [Swerve Subsytem file](https://github.com/Chicago-Robotics-Alliance/2025_CRA_Commons/blob/main/src/main/java/frc/robot/subsystems/swervedrive/SwerveSubsystem.java)

Important lines to take a look at are lines 71, 108-109, 147-157

---
## Troubleshooting
Most problems can be solved by putting print statements before and after setting the motors in the periodic function.

---
## How to tune PID values?
Here are a bunch of documents already made.
- [in general](https://docs.wpilib.org/en/2020/docs/software/advanced-control/introduction/tuning-pid-controller.html)
- [swerve](https://docs.yagsl.com/configuring-yagsl/how-to-tune-pidf)
