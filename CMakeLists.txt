cmake_minimum_required(VERSION 2.8.3)

project(intensity_map_msgs)

find_package(catkin REQUIRED COMPONENTS 
		cmake_modules 
		message_generation
		geometry_msgs 
		std_msgs
	    )

include_directories(include ${catkin_INCLUDE_DIRS})

add_message_files(
  DIRECTORY msg
  FILES
  IntensityMarker.msg)
generate_messages(DEPENDENCIES std_msgs geometry_msgs)


catkin_package(
		CATKIN_DEPENDS message_runtime std_msgs geometry_msgs
	     )



