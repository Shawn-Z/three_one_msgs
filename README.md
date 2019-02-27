## msg structure
three_one_msgs
├── CMakeLists.txt
├── msg
│   ├── control.msg
│   ├── control_speed.msg
│   ├── control_steer.msg
│   ├── control_suspension.msg
│   ├── rawdata_recv.msg
│   ├── rawdata_send.msg
│   ├── report_control_data.msg
│   ├── report_cylinder_position.msg
│   ├── report_cylinder_pressure.msg
│   ├── report_distance.msg
│   ├── report_give_back.msg
│   ├── report_motion.msg
│   ├── report.msg
│   ├── report_torque.msg
│   └── report_vehicle_state.msg
├── package.xml
└── readme.md

## msg file descriptions
1. The file "control.msg" can control all of the function of the car.
2. The files with prefix of "control_"(eg. "control_speed.msg") can control part of the function of the car.
3. The file "report.msg" contains feedbacks of the car, and it is composed of files with prefix "report_". For now, testing on 6t, feedbacks are mainly contained in "report_motion.msg".
