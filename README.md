# Mapping
Devices take data from sensors to build a picture of the environment around them and where they are positioned within that environment.

### External sensors
* Camera or Laser scanner

### Internal sensors
* Tires (Wheel Encoder) 
  * There will be black and white strives in the wheels of the Tires.
### Study Cases
* Laser Scanner with SLAM
  * SLAM is concerned with the problem of building a map of unknown environment by a mobile robot while at the same time navigating the environment using the map.
  * It is applicable for both 2D and 3D motion.
  * Hardware requires:
    * A mobile robot
    * Range measurement device (Laser scanner for our case.)
  * Software requirements(steps):
    * First we installed Windows Subsystem for Linux (WSL) for running linux binary executables on windows 10.
    * Then we wrote the command sudo apt install git in the ubuntu command prompt to install the git.
    * Then we clone the openslam_gmapping repo into our pc using the command git clone (repo url). After that we entered openslam_gmapping folder and run ./configure script for execution.
    * Next run the command sudu apt update to updating repositories to get information on the newest versions of packages and their dependencies.
    * After that we installed the compiler using the command sudu apt-get install build-essential.
    * Then run the command apt-get install qt5-default to get Qt5 development defaults packages.
    * After that install firefox using the command sudu apt install firefox and also run ./configure for execution.
    * Next we downloaded qt3 that is qt-x11-free-3.3.8.tar.bz2 using the command wget (url) and then extract the file using the command tar xvfj (archivename).
    * Next we will be download and install carmen (Carnegie Mellon Robot Navigation Toolkit).
    
    
  * SLAM Process (Consist of number of steps):
    * Laser Data: Obtain data about the surroundings of the robot. 
    * Odometry Data: The goal of the odometry data is to provide an approximate position of the robot as measured by the movement of the wheels of the robot, to serve as the initial guess of where the robot might be in the EKF.
    * Landmarks: Landmarks are the features which can easily be re-observed and distinguished from the environment.
    * Landmark Extraction: Once we have decided on what landmarks a robot should utilize we need to be able to somehow reliable extract them from the robots sensory inputs. Technique for landmark extraction are Spike, RANSAC etc.
    * Data Association: Matching observed landmarks from different (laser) scans with each other.
    * The EKF: Extended Kalman Filter is used to estimate the position of the robot from odometry data and landmark observations. It is  also called the heart of the SLAM process.
    
* Gmapping
  * Gmapping is a highly efficient Rao-Blackwellized partice filter to learn grid maps from laser range data.

### More Study Cases
* Rotary encoder and how they work?
  * An electro-mechanical device that converts the angular position or motion of a shaft or axle to analog or digital output signals.
  * There are two main types of rotary encoder: absolute and incremental.
  * The output of an absolute encoder indicates the current shaft position, making it an angle transducer.
  * The output of an incremental encoder provides information about the motion of the shaft, which typically is processed elsewhere into information such as position, speed and distance.
 
