Code Book
=========

Introduction
------------
This is the codebook for `T-data.txt`. 

Data Source
-----------
The raw data input for this script can be
downloaded from [here](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip).

Description of Data
-------------------
More details of the data set can be found on the original site
linked above.  Briefly, this data consists of accelerometer
data measured using smartphones for a set of 30 subjects in the
age range 19-48 years performing various activities
(walking, walking up stairs, walking down stairs, sitting, standing,
and laying).  The accelerometer measured 3-axis acceleration
and 3-axis angular acceleration at 50 Hz.  The data were low-pass
filtered to remove noise, and acceleration due to gravity was
removed.  Measurements are presented in the time domain,
and, in some cases, the frequency domain.  Note that each variable has been
rescaled to the range [-1, 1].

#### Description of each variable
The time domain measurements are prefaced with Time., the frequency
domain ones with Freq.  For each variable, the Mean and Standard
Deviation are provided (Mean and Sd, respectively).  All measurement
variables come in 3 versions (X, Y, Z) representing the three axes of
motion (both linear and angular).  The tidy dataset consists of the
mean values for each subject performing each activity of the mean and
standard deviation of each variable, along with the subject id and
activity type.  So, for example, Time.BodyAcc.Mean.X is the
time-domain mean acceleration along the X axis, which has been further
averaged over all of the measurement sets for each subject performing
a particular activity.

The following features are included, where [t|f] means
time or frequency, [XYZ] means one of X, Y, Z, and [mean|std] means
one of mean or sd:

* activity		The activity type (WALKING, WALKING\_UPSTAIRS,
  			WALKING\_DOWNSTAIRS, SITTING, STANDING, LAYING)
* subject.id        The subject ID number (1 to 30, inclusive)
* [t|f]BodyAcc_[mean|std]_[XYZ]  Body acceleration, linear,
    with the effects of gravity removed
* [t|f]GravityAcc_[mean|std]_[XYZ]  Gravitational acceleration, 
    linear
* [t|f]BodyAccJerk_[mean|std]_[XYZ]  Body jerk, linear
    (derivative of acceleration)
* [t|f]BodyGyro_[mean|std]_[XYZ] Angular velocity along
     each gyroscopic axis
* [t|f]BodyGyroAcc_[mean|std]_[XYZ] Angular acceleration along
     each gyroscopic axis
* [t|f]BodyAccMag_[mean|std] Mean magnitude of linear body
   acceleration (euclidean norm of body [XYZ] acceleration, gravity 
   removed)
* [t|f]GravityAccMag_[mean|std] Mean magnitude of gravitational 
    acceleration (euclidean norm)
* [t|f]BodyAccJerkMag_[mean|std] Mean magnitude of linear body
   jerk (euclidean norm of body [XYZ] jerk)
* [t|f]BodyGyroMag_[mean|std] Mean magnitude of angular body
   velocity (euclidean norm of body [XYZ] angular velocity)
* [t|f]BodyGyroAccMag_[mean|std] Mean magnitude of angular body
   acceleration (euclidean norm of body [XYZ] angular velocity)

#### Units
Because each physical variable has been rescaled to the range [-1, 1],
they have been rendered unitless.
