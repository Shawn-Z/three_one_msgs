## msg file structure
three_one_msgs  
├── CMakeLists.txt  
├── msg  
│   ├── control.msg    &emsp;# total control of the car  
│   ├── control_speed.msg    &emsp;# control the speed of the car  
│   ├── control_steer.msg    &emsp;# control the steer of the car  
│   ├── control_suspension.msg    &emsp;# control the suspension of the car  
│   ├── rawdata_recv.msg    &emsp;# udp receive rawdata for the car  
│   ├── rawdata_send.msg    &emsp;# udp send rawdata to the car  
│   ├── report_control_data.msg    &emsp;# feedback of control data from `ecu_communication`, for comparation and analysis  
│   ├── report_cylinder_position.msg    &emsp;# feedback of cyclinder position  
│   ├── report_cylinder_pressure.msg    &emsp;# feedback of cyclinder pressure  
│   ├── report_distance.msg    &emsp;# feedback of mileage and pulse counter  
│   ├── report_give_back.msg    &emsp;# feedback of control data from ecu  
│   ├── report_motion.msg    &emsp;# feedback speed info of the car  
│   ├── report.msg    &emsp;# total feedback of the car  
│   ├── report_torque.msg    &emsp;# feedback of torque  
│   └── report_vehicle_state.msg    &emsp;# feedback of functions, such as light, ring.  
├── package.xml  
└── readme.md  

## structure of `control.msg`
uint8 priority  
three_one_msgs/control_speed speed  
  uint8 priority  
  uint8 halt  
  uint8 gear  
  float32 speed  
three_one_msgs/control_steer steer  
  uint8 priority  
  float64 curvature  
three_one_msgs/control_suspension suspension  
  uint8 priority  
  uint8 cylinder_select  
  uint8 suspension_select  
  uint8 suspension_work_mode  
  uint8 suspension_work_mode_detail  
  uint8 suspension_cylinder_select_mode  
  uint8 suspension_cylinder_motor_control  
  uint8 vertical_wall_mode  
  uint8 fix_two_chamber_valve  


## msg file descriptions
1. The file "control.msg" can control all of the function of the car.
2. The files with prefix of "control_"(eg. "control_speed.msg") can control part of the function of the car.
3. The file "report.msg" contains feedbacks of the car, and it is composed of files with prefix "report_". For now, testing on 6t, feedbacks are mainly contained in "report_motion.msg".
