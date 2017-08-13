<p class="p1"><span class="s1"></span><br></p>
<h1 style="margin: 0.0px 0.0px 14.9px 0.0px; line-height: 22.0px; font: 18.0px Times; color: #000000; -webkit-text-stroke: #000000"><span class="s1"><b>Getting and Cleaning Data Project</b></span></h1>
<h2 style="margin: 0.0px 0.0px 14.9px 0.0px; line-height: 22.0px; font: 18.0px Times; color: #000000; -webkit-text-stroke: #000000"><span class="s1"><b>run_analysis.R</b></span></h2>
<p class="p3"><span class="s1">The cleanup script (run_analysis.R) does the following:</span></p>
<ol class="ol1">
  <li class="li4"><span class="s2"></span><span class="s1">Merges the training and the test sets to create one data set.</span></li>
  <li class="li4"><span class="s2"></span><span class="s1">Extracts only the measurements on the mean and standard deviation for each measurement.</span></li>
  <li class="li4"><span class="s2"></span><span class="s1">Uses descriptive activity names to name the activities in the data set</span></li>
  <li class="li4"><span class="s2"></span><span class="s1">Appropriately labels the data set with descriptive activity names.</span></li>
  <li class="li4"><span class="s2"></span><span class="s1">Creates a second, independent tidy data set with the average of each variable for each activity and each subject.</span></li>
</ol>
<h2 style="margin: 0.0px 0.0px 14.9px 0.0px; line-height: 22.0px; font: 18.0px Times; color: #000000; -webkit-text-stroke: #000000"><span class="s1"><b>Running the script</b></span></h2>
<p class="p5"><span class="s1">Run the function <b>run_analysis()</b></span></p>
<p class="p6"><span class="s1"><span class="Apple-converted-space"> </span></span></p>
<h2 style="margin: 0.0px 0.0px 14.9px 0.0px; line-height: 22.0px; font: 18.0px Times; color: #000000; -webkit-text-stroke: #000000"><span class="s1"><b>Process</b></span></h2>
<ol class="ol1">
  <li class="li4"><span class="s2"></span><span class="s1">For both the test and train datasets, produce an interim dataset:</span></li>
  <ol class="ol1">
    <li class="li4"><span class="s2"></span><span class="s1">Extract the mean and standard deviation features (listed in CodeBook.md, section 'Extracted Features'). This is the </span><span class="s3">values</span><span class="s1"> table.</span></li>
    <li class="li4"><span class="s2"></span><span class="s1">Get the list of activities.</span></li>
    <li class="li4"><span class="s2"></span><span class="s1">Put the activity <i>labels</i> (not numbers) into the </span><span class="s3">values</span><span class="s1"> table.</span></li>
    <li class="li4"><span class="s2"></span><span class="s1">Get the list of subjects.</span></li>
    <li class="li4"><span class="s2"></span><span class="s1">Put the subject IDs into the </span><span class="s3">values</span><span class="s1"> table.</span></li>
  </ol>
  <li class="li4"><span class="s2"></span><span class="s1">Join the test and train interim datasets.</span></li>
  <li class="li4"><span class="s2"></span><span class="s1">Put each variable on its own row.</span></li>
  <li class="li4"><span class="s2"></span><span class="s1">Rejoin the entire table, keying on subject/acitivity pairs, applying the mean function to each vector of values in each subject/activity pair. This is the clean dataset.</span></li>
  <li class="li4"><span class="s2"></span><span class="s1">Write the clean dataset to disk.</span></li>
</ol>
<h2 style="margin: 0.0px 0.0px 14.9px 0.0px; line-height: 22.0px; font: 18.0px Times; color: #000000; -webkit-text-stroke: #000000"><span class="s1"><b>Cleaned Data</b></span></h2>
<p class="p3"><span class="s1">The resulting clean dataset is in this repository tidydata</span><span class="s3">.txt</span><span class="s1">. It contains one row for each subject/activity pair and columns for subject, activity, and each feature that was a mean or standard deviation from the original dataset.</span></p>
<h2 style="margin: 0.0px 0.0px 14.9px 0.0px; line-height: 22.0px; font: 18.0px Times; color: #000000; -webkit-text-stroke: #000000"><span class="s1"><b>Notes</b></span></h2>
<p class="p3"><span class="s1">X_* - feature values (one row of 561 features for a single activity) Y_* - activity identifiers (for each row in X_<i>) subject_</i> - subject identifiers for rows in X_*</span></p>
</body>
</html>
