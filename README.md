# Landmark Detection & Robot Tracking (SLAM)

## Project Overview

This project is all about implementation SLAM (Simultaneous Localization and Mapping) for a 2 dimensional world. Goal is to combine what we know about robot sensor measurements and movement to create a map of an environment from only sensor and motion data gathered by a robot, over time. SLAM gives us a way to track the location of a robot in the world in real-time and identify the locations of landmarks such as buildings, trees, rocks, and other world features. This is an active area of research in the fields of robotics and autonomous systems. 

*Below is an example of a 2D robot world with landmarks (purple x's) and the robot (a red 'o') located and found using *only* sensor and motion data collected by that robot. This is just one example for a 50x50 grid world; in your work you will likely generate a variety of these maps.*

<p align="center">
  <img src="./images/robot_world.png" width=50% height=50% />
</p>

The project will be broken up into three Python notebooks; the first two are for exploration of provided code, and a review of SLAM architectures, **only Notebook 3 and the `robot_class.py` file will be graded**:

__Notebook 1__ : Robot Moving and Sensing

__Notebook 2__ : Omega and Xi, Constraints 

__Notebook 3__ : Landmark Detection and Tracking 

__robot_class.py__ : Robot class with its world parameters

__helpers.py__ : helper functions for making data, world display

## Local Environment Instructions

1. Clone the repository, and navigate to the downloaded folder.
```
git clone https://github.com/Antanskas/SLAM.git
```

2. Create (and activate) a new environment, named `cv-nd` with Python 3.6. If prompted to proceed with the install `(Proceed [y]/n)` type y.

	- __Linux__ or __Mac__: 
	```
	conda create -n cv-nd python=3.6
	source activate cv-nd
	```
	- __Windows__: 
	```
	conda create --name cv-nd python=3.6
	activate cv-nd
	```

6. Install a few required pip packages, which are specified in the requirements text file (including OpenCV).
```
pip install -r requirements.txt
```
To implement Graph SLAM, a matrix and a vector (omega and xi, respectively) are introduced. The matrix is square and labelled with all the robot poses (xi) and all the landmarks (Li).

## Graph SLAM

Every time we make an observation, for example as we move between two poses by some distance dx and can relate those two positions, you can represent this as a numerical relationship in these matrices.

We are referring to robot poses as Px, Py and landmark positions as Lx, Ly, and one way to approach this challenge is to add both x and y locations in the constraint matrices.

<p align="center">
  <img src="images/constraints2D.png" width=50% height=50%>
</p>

LICENSE: This project is licensed under the terms of the MIT license.
