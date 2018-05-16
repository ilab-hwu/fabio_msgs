cmake_minimum_required(VERSION 2.8.3)
project(pepper_actions)

find_package(catkin REQUIRED COMPONENTS
	actionlib 
	actionlib_msgs
	message_generation
	message_runtime
	rospy
	std_msgs
	diagnostic_msgs
)


add_action_files(
	FILES
	CheckPersonExistsAS.action
	DescribeRouteAS.action
	DisengagePersonAS.action
	DisengagedByPersonAS.action
	EngagePersonAS.action
	EngagedByPersonAS.action
	FindPersonAS.action
	FindPromotionTargetAS.action
	PromoteProductAS.action
	ChargeRobotAS.action
	UndockRobotAS.action
	MoveBaseHomeAS.action
	MoveBaseToDistanceAS.action
	MoveBaseToWaypointAS.action
	TalkToPersonAS.action
	RespondToPersonAS.action
	TrackPersonAS.action
)

generate_messages(
	DEPENDENCIES
	std_msgs
	actionlib_msgs
	# ssp_synthesis_msgs
)

catkin_package(
	# INCLUDE_DIRS
	# LIBRARIES
	# CATKIN_DEPENDS
	# DEPENDS
)

include_directories(
	${catkin_INCLUDE_DIRS}
)

