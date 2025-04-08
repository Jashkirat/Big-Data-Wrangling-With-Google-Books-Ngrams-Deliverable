# Big-Data-Wrangling-With-Google-Books-Ngrams-Deliverable

In this assignment, you will apply the skills you've learned in the Big Data Fundamentals unit to load, filter, and visualize a large real-world dataset in a cloud-based distributed computing environment using Hadoop, Spark, Hive, and the S3 filesystem. Prepare a professional report to summarize the findings and be sure to include an appendix with screenshots of the steps completed for Questions 1 and 2.

The Google Ngrams dataset was created by Google's research team by analyzing all of the content in Google Books - these digitized texts represent approximately 4% of all books ever printed, and span a time period from the 1800s into the 2000s.

The scope of data processing and analysis is outlined in the questions below. Please document all your steps and commands/ code; there are several format options to submit both the code and a written report.

Spin up a new EMR cluster on AWS for using Spark and EMR notebooks - follow the same instructions as for the Spark Lab.
Connect to the head node of the cluster using SSH.
Copy the data folder from the S3 bucket directly into a directory on the Hadoop File System (HDFS) named /user/hadoop/eng_1M_1gram.
Using pyspark, read the data you copied into HDFS in Step 3. You may either use Jupyterhub on EMR (the default user and password are jovyan and jupyter) or work from pyspark in the terminal if you prefer. Once you have created a pyspark DataFrame, complete the following steps below:
Describe the dataset (examples include size, shape, schema) in pyspark
Create a new DataFrame from a query using Spark SQL, filtering to include only the rows where the token is "data" and describe the new dataset
Write the filtered data back to a directory in the HDFS from Spark using df.write.csv(). Be sure to pass the header=True parameter and examine the contents of what you've written.
Collect the contents of the directory into a single file on the local drive of the head node using getmerge and move this file into a S3 bucket in your account.
On your local machine (or on AWS outside of Spark) in python, read the CSV data from the S3 folder into a pandas DataFrame (You will have to research how to read data into pandas from S3 buckets). Note You must have first authenticated on your machine using aws configure on the command line to complete this step).
Plot the number of occurrences of the token (the frequency column) of data over the years using matplotlib.
Compare Hadoop and Spark as distributed file systems.
What are the advantages/ differences between Hadoop and Spark? List two advantages for each.
Explain how the HDFS stores the data.
Requirements
For your submission, prepare a professional report communicating the different steps taken and the list of different commands run in your session. The report should include an appendix of screenshots where appropriate. The report should be a PDF document. We should be able to use your report as a tutorial on replicating your work.
The submission should also include a Jupyter notebook for Step 6, as well as potentially a Jupyter notebook on EMR for Step 4.