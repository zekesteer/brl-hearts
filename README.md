# brl-hearts Competition Repository 
(Bristol Robotics Laboratory - Healthcare Engineering and Assistive Robotics Technology and Services)

"The European Robotic League (ERL) is an innovative concept for robot
competitions. The ERL is composed of multiple Local Tournaments, held
in different research labs across Europe, with certified test beds,
and a few competitions as part of Major Tournaments, such as
RoboCup. Teams participate in a minimum of 2 tournaments (Local and/or
Major) per year and get scores based on their performances. A final
end of year score is computed for each team, per Task Benchmark (TBM)
and Functionality Benchmark (FBM), using the best two participation in
tournaments, and teams are ranked based on their final score. Prizes
for the top teams (per TBM and FBM where they have participated) are
awarded during the next year's European Robotics Forum (ERF)."
-https://eu-robotics.net/robotics_league/erl-service/about/index.html

The code in this repository consists of ROS (kinetic) packages written
for the TIAGO robot. The code is divided into general skills
(e.g. speech to text) and specific modules for use during the testing
of the functional and task benchmarks (e.g. fbm1 or tbm2).


Getting started:

1. The Tiago robot does not yet support the most recent versions of
ROS, so you need to install the latest version which is supported.
This is Kinetic Kame, which in turn is not supported by the latest
versions of Ubuntu.

So, you need to install Ubuntu 16.04.

2. Ubuntu 16.04 comes with Lunar Loggerhead ROS in its repositories but
the Tiago robot does not yet support it.  So you need to follow the
instructions at http://wiki.ros.org/kinetic/Installation/Ubuntu to
install ROS Kinetic Kame on your 16.04 system. Both Kinetic ROS and
Ubuntu 16.04 are supported until April 2021.




How to make for computers with issues with face recognition
```
catkin_make --pkg fbm1_object_perception fbm2_navigation hearts_camera_saver hearts_navigation hearts_test_package tbm1_getting_to_know_my_home tbm2_welcoming_visitors brl_ipcam fbm3_speech_understanding hearts_stt hearts_tts python_support_library roah_rsbb_comm_ros hearts_face_uniform hearts_webcam speech_recognition
```
OR
```
catkin_make -DCATKIN_BLACKLIST_PACKAGES="object_perception_2;fbm1_object_perception;hearts_face_uniform_reg;hearts_face_uniform"
```
