<h1 style="margin: 0.0px 0.0px 10.0px 0.0px; line-height: 40.0px; font: 38.5px 'Helvetica Neue'; color: #333333; -webkit-text-stroke: #333333"><span class="s1"><b>CODEBOOK.md</b></span></h1>
<h1 style="margin: 0.0px 0.0px 10.0px 0.0px; line-height: 40.0px; font: 38.5px 'Helvetica Neue'; color: #333333; -webkit-text-stroke: #333333"><span class="s1"><b>Getting and Cleaning Data Course Project</b></span></h1>
<p class="p2"><span class="s1">Instructions for project The purpose of this project is to demonstrate your ability to collect, work with, and clean a data set. The goal is to prepare tidy data that can be used for later analysis. You will be graded by your peers on a series of yes/no questions related to the project. You will be required to submit: 1) a tidy data set as described below, 2) a link to a Github repository with your script for performing the analysis, and 3) a code book that describes the variables, the data, and any transformations or work that you performed to clean up the data called CodeBook.md. You should also include a README.md in the repo with your scripts. This repo explains how all of the scripts work and how they are connected.</span></p>
<p class="p2"><span class="s1">One of the most exciting areas in all of data science right now is wearable computing - see for example this article . Companies like Fitbit, Nike, and Jawbone Up are racing to develop the most advanced algorithms to attract new users. The data linked to from the course website represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained:</span></p>
<p class="p3"><span class="s1"><a href="http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones">http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones<span class="s2"></span></a></span></p>
<p class="p2"><span class="s1">Here are the data for the project:</span></p>
<p class="p3"><span class="s1"><a href="https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip">https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip<span class="s2"></span></a></span></p>
<p class="p2"><span class="s1">You should create one R script called run_analysis.R that does the following.</span></p>
<ol class="ol1">
  <li class="li4"><span class="s3"></span><span class="s1">Merges the training and the test sets to create one data set.</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Extracts only the measurements on the mean and standard deviation for each measurement.</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Uses descriptive activity names to name the activities in the data set</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Appropriately labels the data set with descriptive variable names.</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.</span></li>
</ol>
<h3 style="margin: 0.0px 0.0px 10.0px 0.0px; line-height: 40.0px; font: 24.5px 'Helvetica Neue'; color: #333333; -webkit-text-stroke: #333333"><span class="s1"><b>Description of the DATA</b></span></h3>
<p class="p2"><span class="s1">The features selected for this database come from the accelerometer and gyroscope 3-axial raw signals tAcc-XYZ and tGyro-XYZ. These time domain signals (prefix ‘t’ to denote time) were captured at a constant rate of 50 Hz. and the acceleration signal was then separated into body and gravity acceleration signals (tBodyAcc-XYZ and tGravityAcc-XYZ) – both using a low pass Butterworth filter.</span></p>
<p class="p2"><span class="s1">The body linear acceleration and angular velocity were derived in time to obtain Jerk signals (tBodyAccJerk-XYZ and tBodyGyroJerk-XYZ). Also the magnitude of these three-dimensional signals were calculated using the Euclidean norm (tBodyAccMag, tGravityAccMag, tBodyAccJerkMag, tBodyGyroMag, tBodyGyroJerkMag).</span></p>
<p class="p2"><span class="s1">A Fast Fourier Transform (FFT) was applied to some of these signals producing fBodyAcc-XYZ, fBodyAccJerk-XYZ, fBodyGyro-XYZ, fBodyAccJerkMag, fBodyGyroMag, fBodyGyroJerkMag. (<i>Note the ‘f’ to indicate frequency domain signals</i>).</span></p>
<h5 style="margin: 0.0px 0.0px 10.0px 0.0px; line-height: 20.0px; font: 14.0px 'Helvetica Neue'; color: #333333; -webkit-text-stroke: #333333"><span class="s1"><b>Description of abbreviations of measurements</b></span></h5>
<ol class="ol1">
  <li class="li4"><span class="s3"></span><span class="s1">leading t or f is based on time or frequency measurements.</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Body = related to body movement.</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Gravity = acceleration of gravity</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Acc = accelerometer measurement</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Gyro = gyroscopic measurements</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Jerk = sudden movement acceleration</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Mag = magnitude of movement</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">mean and SD are calculated for each subject for each activity for each mean and SD measurements.</span></li>
</ol>
<p class="p2"><span class="s1">The units given are g’s for the accelerometer and rad/sec for the gyro and g/sec and rad/sec/sec for the corresponding jerks.</span></p>
<p class="p2"><span class="s1">These signals were used to estimate variables of the feature vector for each pattern:<br>
‘-XYZ’ is used to denote 3-axial signals in the X, Y and Z directions. They total 33 measurements including the 3 dimensions - the X,Y, and Z axes.</span></p>
<ul class="ul1">
  <li class="li4"><span class="s3"></span><span class="s1">tBodyAcc-XYZ</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">tGravityAcc-XYZ</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">tBodyAccJerk-XYZ</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">tBodyGyro-XYZ</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">tBodyGyroJerk-XYZ</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">tBodyAccMag</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">tGravityAccMag</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">tBodyAccJerkMag</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">tBodyGyroMag</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">tBodyGyroJerkMag</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">fBodyAcc-XYZ</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">fBodyAccJerk-XYZ</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">fBodyGyro-XYZ</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">fBodyAccMag</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">fBodyAccJerkMag</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">fBodyGyroMag</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">fBodyGyroJerkMag</span></li>
</ul>
<h5 style="margin: 0.0px 0.0px 10.0px 0.0px; line-height: 20.0px; font: 14.0px 'Helvetica Neue'; color: #333333; -webkit-text-stroke: #333333"><span class="s1"><b>The set of variables that were estimated from these signals are:</b></span></h5>
<ul class="ul1">
  <li class="li4"><span class="s3"></span><span class="s1">mean(): Mean value</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">std(): Standard deviation</span></li>
</ul>
<h3 style="margin: 0.0px 0.0px 10.0px 0.0px; line-height: 40.0px; font: 24.5px 'Helvetica Neue'; color: #333333; -webkit-text-stroke: #333333"><span class="s1"><b>Data Set Information:</b></span></h3>
<p class="p2"><span class="s1">The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.</span></p>
<p class="p2"><span class="s1">The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.</span></p>
<h4 style="margin: 0.0px 0.0px 10.0px 0.0px; line-height: 20.0px; font: 17.5px 'Helvetica Neue'; color: #333333; -webkit-text-stroke: #333333"><span class="s1"><b>Files in folder ‘UCI HAR Dataset’ that will be used are:</b></span></h4>
<ol class="ol1">
  <li class="li4"><span class="s3"></span><span class="s1">SUBJECT FILES</span></li>
</ol>
<ul class="ul1">
  <ul class="ul2">
    <li class="li4"><span class="s3"></span><span class="s1">test/subject_test.txt</span></li>
    <li class="li4"><span class="s3"></span><span class="s1">train/subject_train.txt</span></li>
  </ul>
</ul>
<ol class="ol1">
  <li class="li4"><span class="s3"></span><span class="s1">ACTIVITY FILES</span></li>
</ol>
<ul class="ul1">
  <ul class="ul2">
    <li class="li4"><span class="s3"></span><span class="s1">test/X_test.txt</span></li>
    <li class="li4"><span class="s3"></span><span class="s1">train/X_train.txt</span></li>
  </ul>
</ul>
<ol class="ol1">
  <li class="li4"><span class="s3"></span><span class="s1">DATA FILES</span></li>
</ol>
<ul class="ul1">
  <ul class="ul2">
    <li class="li4"><span class="s3"></span><span class="s1">test/y_test.txt</span></li>
    <li class="li4"><span class="s3"></span><span class="s1">train/y_train.txt</span></li>
  </ul>
</ul>
<ol class="ol1">
  <li class="li2"><span class="s3"></span><span class="s1">features.txt - Names of column variables in the dataTable</span></li>
  <li class="li2"><span class="s3"></span><span class="s1">activity_labels.txt - Links the class labels with their activity name.<br>
</span></li>
</ol>
<h3 style="margin: 0.0px 0.0px 10.0px 0.0px; line-height: 40.0px; font: 24.5px 'Helvetica Neue'; color: #333333; -webkit-text-stroke: #333333"><span class="s1"><b>Appropriately labels the data set with descriptive variable names.</b></span></h3>
<ol class="ol1">
  <li class="li4"><span class="s3"></span><span class="s1">leading t or f is based on time or frequency measurements.</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Body = related to body movement.</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Gravity = acceleration of gravity</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Acc = accelerometer measurement</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Gyro = gyroscopic measurements</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Jerk = sudden movement acceleration</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">Mag = magnitude of movement</span></li>
  <li class="li4"><span class="s3"></span><span class="s1">mean and SD are calculated for each subject for each activity for each mean and SD measurements. The units given are g’s for the accelerometer and rad/sec for the gyro and g/sec and rad/sec/sec for the corresponding jerks.</span></li>
</ol>
<p class="p7"><span class="s1">#Names before</span></p>
<p class="p7"><span class="s1">head(str(dataTable),2)</span></p>
<p class="p8"><span class="s1">## Classes 'tbl_df', 'tbl' and 'data.frame':<span class="Apple-converted-space">    </span>180 obs. of<span class="Apple-converted-space">  </span>69 variables:</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ subject<span class="Apple-converted-space">                    </span>: int<span class="Apple-converted-space">  </span>1 1 1 1 1 1 2 2 2 2 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ activityName <span class="Apple-converted-space">              </span>: chr<span class="Apple-converted-space">  </span>"LAYING" "SITTING" "STANDING" "WALKING" ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ activityNum<span class="Apple-converted-space">                </span>: num<span class="Apple-converted-space">  </span>6 4 5 1 3 2 6 4 5 1 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAcc-mean()-X<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>0.222 0.261 0.279 0.277 0.289 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAcc-mean()-Y<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.04051 -0.00131 -0.01614 -0.01738 -0.00992 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAcc-mean()-Z<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.113 -0.105 -0.111 -0.111 -0.108 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAcc-std()-X <span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.928 -0.977 -0.996 -0.284 0.03 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAcc-std()-Y <span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.8368 -0.9226 -0.9732 0.1145 -0.0319 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAcc-std()-Z <span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.826 -0.94 -0.98 -0.26 -0.23 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tGravityAcc-mean()-X <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.249 0.832 0.943 0.935 0.932 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tGravityAcc-mean()-Y <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>0.706 0.204 -0.273 -0.282 -0.267 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tGravityAcc-mean()-Z <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>0.4458 0.332 0.0135 -0.0681 -0.0621 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tGravityAcc-std()-X<span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.897 -0.968 -0.994 -0.977 -0.951 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tGravityAcc-std()-Y<span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.908 -0.936 -0.981 -0.971 -0.937 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tGravityAcc-std()-Z<span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.852 -0.949 -0.976 -0.948 -0.896 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAccJerk-mean()-X<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>0.0811 0.0775 0.0754 0.074 0.0542 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAccJerk-mean()-Y<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>0.003838 -0.000619 0.007976 0.028272 0.02965 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAccJerk-mean()-Z<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>0.01083 -0.00337 -0.00369 -0.00417 -0.01097 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAccJerk-std()-X <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.9585 -0.9864 -0.9946 -0.1136 -0.0123 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAccJerk-std()-Y <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.924 -0.981 -0.986 0.067 -0.102 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAccJerk-std()-Z <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.955 -0.988 -0.992 -0.503 -0.346 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyro-mean()-X <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.0166 -0.0454 -0.024 -0.0418 -0.0351 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyro-mean()-Y <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.0645 -0.0919 -0.0594 -0.0695 -0.0909 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyro-mean()-Z <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>0.1487 0.0629 0.0748 0.0849 0.0901 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyro-std()-X<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.874 -0.977 -0.987 -0.474 -0.458 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyro-std()-Y<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.9511 -0.9665 -0.9877 -0.0546 -0.1263 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyro-std()-Z<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.908 -0.941 -0.981 -0.344 -0.125 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyroJerk-mean()-X <span class="Apple-converted-space">    </span>: num<span class="Apple-converted-space">  </span>-0.1073 -0.0937 -0.0996 -0.09 -0.074 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyroJerk-mean()-Y <span class="Apple-converted-space">    </span>: num<span class="Apple-converted-space">  </span>-0.0415 -0.0402 -0.0441 -0.0398 -0.044 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyroJerk-mean()-Z <span class="Apple-converted-space">    </span>: num<span class="Apple-converted-space">  </span>-0.0741 -0.0467 -0.049 -0.0461 -0.027 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyroJerk-std()-X<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.919 -0.992 -0.993 -0.207 -0.487 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyroJerk-std()-Y<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.968 -0.99 -0.995 -0.304 -0.239 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyroJerk-std()-Z<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.958 -0.988 -0.992 -0.404 -0.269 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAccMag-mean() <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.8419 -0.9485 -0.9843 -0.137 0.0272 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAccMag-std()<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.7951 -0.9271 -0.9819 -0.2197 0.0199 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tGravityAccMag-mean()<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.8419 -0.9485 -0.9843 -0.137 0.0272 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tGravityAccMag-std() <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.7951 -0.9271 -0.9819 -0.2197 0.0199 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAccJerkMag-mean() <span class="Apple-converted-space">    </span>: num<span class="Apple-converted-space">  </span>-0.9544 -0.9874 -0.9924 -0.1414 -0.0894 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyAccJerkMag-std()<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.9282 -0.9841 -0.9931 -0.0745 -0.0258 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyroMag-mean()<span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.8748 -0.9309 -0.9765 -0.161 -0.0757 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyroMag-std() <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.819 -0.935 -0.979 -0.187 -0.226 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyroJerkMag-mean()<span class="Apple-converted-space">    </span>: num<span class="Apple-converted-space">  </span>-0.963 -0.992 -0.995 -0.299 -0.295 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ tBodyGyroJerkMag-std() <span class="Apple-converted-space">    </span>: num<span class="Apple-converted-space">  </span>-0.936 -0.988 -0.995 -0.325 -0.307 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAcc-mean()-X<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.9391 -0.9796 -0.9952 -0.2028 0.0382 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAcc-mean()-Y<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.86707 -0.94408 -0.97707 0.08971 0.00155 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAcc-mean()-Z<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.883 -0.959 -0.985 -0.332 -0.226 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAcc-std()-X <span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.9244 -0.9764 -0.996 -0.3191 0.0243 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAcc-std()-Y <span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.834 -0.917 -0.972 0.056 -0.113 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAcc-std()-Z <span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.813 -0.934 -0.978 -0.28 -0.298 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAccJerk-mean()-X<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.9571 -0.9866 -0.9946 -0.1705 -0.0277 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAccJerk-mean()-Y<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.9225 -0.9816 -0.9854 -0.0352 -0.1287 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAccJerk-mean()-Z<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.948 -0.986 -0.991 -0.469 -0.288 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAccJerk-std()-X <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.9642 -0.9875 -0.9951 -0.1336 -0.0863 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAccJerk-std()-Y <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.932 -0.983 -0.987 0.107 -0.135 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAccJerk-std()-Z <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.961 -0.988 -0.992 -0.535 -0.402 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyGyro-mean()-X <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.85 -0.976 -0.986 -0.339 -0.352 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyGyro-mean()-Y <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.9522 -0.9758 -0.989 -0.1031 -0.0557 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyGyro-mean()-Z <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.9093 -0.9513 -0.9808 -0.2559 -0.0319 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyGyro-std()-X<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.882 -0.978 -0.987 -0.517 -0.495 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyGyro-std()-Y<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.9512 -0.9623 -0.9871 -0.0335 -0.1814 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyGyro-std()-Z<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.917 -0.944 -0.982 -0.437 -0.238 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAccMag-mean() <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.8618 -0.9478 -0.9854 -0.1286 0.0966 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyAccMag-std()<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.798 -0.928 -0.982 -0.398 -0.187 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyBodyAccJerkMag-mean() : num<span class="Apple-converted-space">  </span>-0.9333 -0.9853 -0.9925 -0.0571 0.0262 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyBodyAccJerkMag-std()<span class="Apple-converted-space">  </span>: num<span class="Apple-converted-space">  </span>-0.922 -0.982 -0.993 -0.103 -0.104 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyBodyGyroMag-mean()<span class="Apple-converted-space">    </span>: num<span class="Apple-converted-space">  </span>-0.862 -0.958 -0.985 -0.199 -0.186 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyBodyGyroMag-std() <span class="Apple-converted-space">    </span>: num<span class="Apple-converted-space">  </span>-0.824 -0.932 -0.978 -0.321 -0.398 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyBodyGyroJerkMag-mean(): num<span class="Apple-converted-space">  </span>-0.942 -0.99 -0.995 -0.319 -0.282 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ fBodyBodyGyroJerkMag-std() : num<span class="Apple-converted-space">  </span>-0.933 -0.987 -0.995 -0.382 -0.392 ...</span></p>
<p class="p8"><span class="s1">## NULL</span></p>
<p class="p7"><span class="s1">head(str(dataTable),6)</span></p>
<p class="p8"><span class="s1">## Classes 'tbl_df', 'tbl' and 'data.frame':<span class="Apple-converted-space">    </span>180 obs. of<span class="Apple-converted-space">  </span>69 variables:</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ subject <span class="Apple-converted-space">                                      </span>: int<span class="Apple-converted-space">  </span>1 1 1 1 1 1 2 2 2 2 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ activityName<span class="Apple-converted-space">                                  </span>: chr<span class="Apple-converted-space">  </span>"LAYING" "SITTING" "STANDING" "WALKING" ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ activityNum <span class="Apple-converted-space">                                  </span>: num<span class="Apple-converted-space">  </span>6 4 5 1 3 2 6 4 5 1 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometer-MEAN()-X<span class="Apple-converted-space">                </span>: num<span class="Apple-converted-space">  </span>0.222 0.261 0.279 0.277 0.289 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometer-MEAN()-Y<span class="Apple-converted-space">                </span>: num<span class="Apple-converted-space">  </span>-0.04051 -0.00131 -0.01614 -0.01738 -0.00992 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometer-MEAN()-Z<span class="Apple-converted-space">                </span>: num<span class="Apple-converted-space">  </span>-0.113 -0.105 -0.111 -0.111 -0.108 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometer-SD()-X<span class="Apple-converted-space">                  </span>: num<span class="Apple-converted-space">  </span>-0.928 -0.977 -0.996 -0.284 0.03 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometer-SD()-Y<span class="Apple-converted-space">                  </span>: num<span class="Apple-converted-space">  </span>-0.8368 -0.9226 -0.9732 0.1145 -0.0319 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometer-SD()-Z<span class="Apple-converted-space">                  </span>: num<span class="Apple-converted-space">  </span>-0.826 -0.94 -0.98 -0.26 -0.23 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeGravityAccelerometer-MEAN()-X <span class="Apple-converted-space">            </span>: num<span class="Apple-converted-space">  </span>-0.249 0.832 0.943 0.935 0.932 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeGravityAccelerometer-MEAN()-Y <span class="Apple-converted-space">            </span>: num<span class="Apple-converted-space">  </span>0.706 0.204 -0.273 -0.282 -0.267 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeGravityAccelerometer-MEAN()-Z <span class="Apple-converted-space">            </span>: num<span class="Apple-converted-space">  </span>0.4458 0.332 0.0135 -0.0681 -0.0621 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeGravityAccelerometer-SD()-X <span class="Apple-converted-space">              </span>: num<span class="Apple-converted-space">  </span>-0.897 -0.968 -0.994 -0.977 -0.951 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeGravityAccelerometer-SD()-Y <span class="Apple-converted-space">              </span>: num<span class="Apple-converted-space">  </span>-0.908 -0.936 -0.981 -0.971 -0.937 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeGravityAccelerometer-SD()-Z <span class="Apple-converted-space">              </span>: num<span class="Apple-converted-space">  </span>-0.852 -0.949 -0.976 -0.948 -0.896 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometerJerk-MEAN()-X<span class="Apple-converted-space">            </span>: num<span class="Apple-converted-space">  </span>0.0811 0.0775 0.0754 0.074 0.0542 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometerJerk-MEAN()-Y<span class="Apple-converted-space">            </span>: num<span class="Apple-converted-space">  </span>0.003838 -0.000619 0.007976 0.028272 0.02965 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometerJerk-MEAN()-Z<span class="Apple-converted-space">            </span>: num<span class="Apple-converted-space">  </span>0.01083 -0.00337 -0.00369 -0.00417 -0.01097 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometerJerk-SD()-X<span class="Apple-converted-space">              </span>: num<span class="Apple-converted-space">  </span>-0.9585 -0.9864 -0.9946 -0.1136 -0.0123 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometerJerk-SD()-Y<span class="Apple-converted-space">              </span>: num<span class="Apple-converted-space">  </span>-0.924 -0.981 -0.986 0.067 -0.102 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometerJerk-SD()-Z<span class="Apple-converted-space">              </span>: num<span class="Apple-converted-space">  </span>-0.955 -0.988 -0.992 -0.503 -0.346 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscope-MEAN()-X<span class="Apple-converted-space">                    </span>: num<span class="Apple-converted-space">  </span>-0.0166 -0.0454 -0.024 -0.0418 -0.0351 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscope-MEAN()-Y<span class="Apple-converted-space">                    </span>: num<span class="Apple-converted-space">  </span>-0.0645 -0.0919 -0.0594 -0.0695 -0.0909 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscope-MEAN()-Z<span class="Apple-converted-space">                    </span>: num<span class="Apple-converted-space">  </span>0.1487 0.0629 0.0748 0.0849 0.0901 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscope-SD()-X<span class="Apple-converted-space">                      </span>: num<span class="Apple-converted-space">  </span>-0.874 -0.977 -0.987 -0.474 -0.458 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscope-SD()-Y<span class="Apple-converted-space">                      </span>: num<span class="Apple-converted-space">  </span>-0.9511 -0.9665 -0.9877 -0.0546 -0.1263 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscope-SD()-Z<span class="Apple-converted-space">                      </span>: num<span class="Apple-converted-space">  </span>-0.908 -0.941 -0.981 -0.344 -0.125 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscopeJerk-MEAN()-X<span class="Apple-converted-space">                </span>: num<span class="Apple-converted-space">  </span>-0.1073 -0.0937 -0.0996 -0.09 -0.074 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscopeJerk-MEAN()-Y<span class="Apple-converted-space">                </span>: num<span class="Apple-converted-space">  </span>-0.0415 -0.0402 -0.0441 -0.0398 -0.044 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscopeJerk-MEAN()-Z<span class="Apple-converted-space">                </span>: num<span class="Apple-converted-space">  </span>-0.0741 -0.0467 -0.049 -0.0461 -0.027 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscopeJerk-SD()-X<span class="Apple-converted-space">                  </span>: num<span class="Apple-converted-space">  </span>-0.919 -0.992 -0.993 -0.207 -0.487 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscopeJerk-SD()-Y<span class="Apple-converted-space">                  </span>: num<span class="Apple-converted-space">  </span>-0.968 -0.99 -0.995 -0.304 -0.239 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscopeJerk-SD()-Z<span class="Apple-converted-space">                  </span>: num<span class="Apple-converted-space">  </span>-0.958 -0.988 -0.992 -0.404 -0.269 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometerMagnitude-MEAN() <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.8419 -0.9485 -0.9843 -0.137 0.0272 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometerMagnitude-SD() <span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.7951 -0.9271 -0.9819 -0.2197 0.0199 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeGravityAccelerometerMagnitude-MEAN()<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.8419 -0.9485 -0.9843 -0.137 0.0272 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeGravityAccelerometerMagnitude-SD()<span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.7951 -0.9271 -0.9819 -0.2197 0.0199 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometerJerkMagnitude-MEAN() <span class="Apple-converted-space">    </span>: num<span class="Apple-converted-space">  </span>-0.9544 -0.9874 -0.9924 -0.1414 -0.0894 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyAccelerometerJerkMagnitude-SD() <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.9282 -0.9841 -0.9931 -0.0745 -0.0258 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscopeMagnitude-MEAN() <span class="Apple-converted-space">            </span>: num<span class="Apple-converted-space">  </span>-0.8748 -0.9309 -0.9765 -0.161 -0.0757 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscopeMagnitude-SD() <span class="Apple-converted-space">              </span>: num<span class="Apple-converted-space">  </span>-0.819 -0.935 -0.979 -0.187 -0.226 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscopeJerkMagnitude-MEAN() <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.963 -0.992 -0.995 -0.299 -0.295 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ timeBodyGyroscopeJerkMagnitude-SD() <span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.936 -0.988 -0.995 -0.325 -0.307 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometer-MEAN()-X <span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.9391 -0.9796 -0.9952 -0.2028 0.0382 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometer-MEAN()-Y <span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.86707 -0.94408 -0.97707 0.08971 0.00155 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometer-MEAN()-Z <span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.883 -0.959 -0.985 -0.332 -0.226 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometer-SD()-X <span class="Apple-converted-space">            </span>: num<span class="Apple-converted-space">  </span>-0.9244 -0.9764 -0.996 -0.3191 0.0243 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometer-SD()-Y <span class="Apple-converted-space">            </span>: num<span class="Apple-converted-space">  </span>-0.834 -0.917 -0.972 0.056 -0.113 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometer-SD()-Z <span class="Apple-converted-space">            </span>: num<span class="Apple-converted-space">  </span>-0.813 -0.934 -0.978 -0.28 -0.298 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometerJerk-MEAN()-X <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.9571 -0.9866 -0.9946 -0.1705 -0.0277 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometerJerk-MEAN()-Y <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.9225 -0.9816 -0.9854 -0.0352 -0.1287 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometerJerk-MEAN()-Z <span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.948 -0.986 -0.991 -0.469 -0.288 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometerJerk-SD()-X <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.9642 -0.9875 -0.9951 -0.1336 -0.0863 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometerJerk-SD()-Y <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.932 -0.983 -0.987 0.107 -0.135 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometerJerk-SD()-Z <span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.961 -0.988 -0.992 -0.535 -0.402 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyGyroscope-MEAN()-X <span class="Apple-converted-space">              </span>: num<span class="Apple-converted-space">  </span>-0.85 -0.976 -0.986 -0.339 -0.352 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyGyroscope-MEAN()-Y <span class="Apple-converted-space">              </span>: num<span class="Apple-converted-space">  </span>-0.9522 -0.9758 -0.989 -0.1031 -0.0557 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyGyroscope-MEAN()-Z <span class="Apple-converted-space">              </span>: num<span class="Apple-converted-space">  </span>-0.9093 -0.9513 -0.9808 -0.2559 -0.0319 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyGyroscope-SD()-X <span class="Apple-converted-space">                </span>: num<span class="Apple-converted-space">  </span>-0.882 -0.978 -0.987 -0.517 -0.495 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyGyroscope-SD()-Y <span class="Apple-converted-space">                </span>: num<span class="Apple-converted-space">  </span>-0.9512 -0.9623 -0.9871 -0.0335 -0.1814 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyGyroscope-SD()-Z <span class="Apple-converted-space">                </span>: num<span class="Apple-converted-space">  </span>-0.917 -0.944 -0.982 -0.437 -0.238 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometerMagnitude-MEAN()<span class="Apple-converted-space">    </span>: num<span class="Apple-converted-space">  </span>-0.8618 -0.9478 -0.9854 -0.1286 0.0966 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometerMagnitude-SD()<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.798 -0.928 -0.982 -0.398 -0.187 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometerJerkMagnitude-MEAN(): num<span class="Apple-converted-space">  </span>-0.9333 -0.9853 -0.9925 -0.0571 0.0262 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyAccelerometerJerkMagnitude-SD()<span class="Apple-converted-space">  </span>: num<span class="Apple-converted-space">  </span>-0.922 -0.982 -0.993 -0.103 -0.104 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyGyroscopeMagnitude-MEAN()<span class="Apple-converted-space">        </span>: num<span class="Apple-converted-space">  </span>-0.862 -0.958 -0.985 -0.199 -0.186 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyGyroscopeMagnitude-SD()<span class="Apple-converted-space">          </span>: num<span class="Apple-converted-space">  </span>-0.824 -0.932 -0.978 -0.321 -0.398 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyGyroscopeJerkMagnitude-MEAN()<span class="Apple-converted-space">    </span>: num<span class="Apple-converted-space">  </span>-0.942 -0.99 -0.995 -0.319 -0.282 ...</span></p>
<p class="p8"><span class="s1">##<span class="Apple-converted-space">  </span>$ frequencyBodyGyroscopeJerkMagnitude-SD()<span class="Apple-converted-space">      </span>: num<span class="Apple-converted-space">  </span>-0.933 -0.987 -0.995 -0.382 -0.392 ...</span></p>
<p class="p8"><span class="s1">## NULL</span></p>
<h3 style="margin: 0.0px 0.0px 10.0px 0.0px; line-height: 40.0px; font: 24.5px 'Helvetica Neue'; color: #333333; -webkit-text-stroke: #333333"><span class="s1"><b>From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.</b></span></h3>
<p class="p9"><span class="s1"></span><br></p>
<p class="p10"><span class="s1">The tidy data set a set of variables for each activity and each subject. 10299 instances are split into 180 groups (30 subjects and 6 activities) and 66 mean and standard deviation features are averaged for each group. The resulting data table has 180 rows and 69 columns – 33 Mean variables + 33 Standard deviation variables + 1 Subject( 1 of of the 30 test subjects) + ActivityName + ActivityNum . The tidy data set’s first row is the header containing the names for each column.</span></p>
</body>
</html>
