cmake_minimum_required(VERSION 2.8.3)
project(three_one_msgs)

add_compile_options(-std=c++11)

find_package(catkin REQUIRED
    COMPONENTS
    message_generation
)

add_message_files(
    DIRECTORY
    msg
    FILES
	control_speed.msg
	control_steer.msg
	control_suspension.msg
	control.msg
	report_motion.msg
	report_torque.msg
	report_distance.msg
	report_vehicle_state.msg
	report_cylinder_position.msg
	report_cylinder_pressure.msg
	report_give_back.msg
	report_control_data.msg
    report.msg
	rawdata_recv.msg
	rawdata_send.msg
)

generate_messages()

catkin_package(
    CATKIN_DEPENDS
    message_runtime
)