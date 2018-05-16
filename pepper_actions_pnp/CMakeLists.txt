cmake_minimum_required(VERSION 2.8.3)
project(pepper_actions_pnp)

find_package(catkin REQUIRED COMPONENTS
	actionlib 
	actionlib_msgs
	message_generation
	message_runtime
	rospy
	std_msgs
	pepper_actions
	pnp_msgs
	diagnostic_msgs
)


add_action_files(
	FILES
	CheckPersonExists.action
	DescribeRoute.action
	DisengagePerson.action
	DisengagedByPerson.action
	EngagePerson.action
	EngagedByPerson.action
	FindPerson.action
	FindPromotionTarget.action
	PromoteProduct.action
	ChargeRobot.action
	UndockRobot.action
	MoveBaseHome.action
	MoveBaseToDistance.action
	MoveBaseToWaypoint.action
	TalkToPerson.action
	RespondToPerson.action
	TrackPerson.action
)

generate_messages(
	DEPENDENCIES
	std_msgs
	actionlib_msgs
	# ssp_synthesis_msgs
	pepper_actions
	pnp_msgs
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

