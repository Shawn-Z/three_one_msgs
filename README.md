## msg structure
three_one_msgs
������ CMakeLists.txt
������ msg
���0�2�0�2 ������ control.msg
���0�2�0�2 ������ control_speed.msg
���0�2�0�2 ������ control_steer.msg
���0�2�0�2 ������ control_suspension.msg
���0�2�0�2 ������ rawdata_recv.msg
���0�2�0�2 ������ rawdata_send.msg
���0�2�0�2 ������ report_control_data.msg
���0�2�0�2 ������ report_cylinder_position.msg
���0�2�0�2 ������ report_cylinder_pressure.msg
���0�2�0�2 ������ report_distance.msg
���0�2�0�2 ������ report_give_back.msg
���0�2�0�2 ������ report_motion.msg
���0�2�0�2 ������ report.msg
���0�2�0�2 ������ report_torque.msg
���0�2�0�2 ������ report_vehicle_state.msg
������ package.xml
������ readme.md

## msg file descriptions
1. The file "control.msg" can control all of the function of the car.
2. The files with prefix of "control_"(eg. "control_speed.msg") can control part of the function of the car.
3. The file "report.msg" contains feedbacks of the car, and it is composed of files with prefix "report_". For now, testing on 6t, feedbacks are mainly contained in "report_motion.msg".
