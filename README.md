# UNCC DSBA 6190 Assignment 3: Cloud Map Reduce and Distributed Jobs

Task Use a distributed computing platform and perform a task suited to the platform. You can demo one of the reference labs or you can implement a custom project (say word count on Spark on AWS EMR).
#
For this assignment I decided to demo the Google qwicklab Distributed Image Processing in Cloud Dataproc
https://www.qwiklabs.com/focuses/5834?catalog_rank=%7B%22rank%22%3A7%2C%22num_filters%22%3A0%2C%22has_search%22%3Atrue%7D&parent=catalog&search_id=4914974

In this demo I learned how to:
1) Create Dataproc clusters, manage them and insatll Apache Spark
2) Ran a job that conducted facial recognition on 3 different images.
#

Step 1: Set up a development machine using Compute engine

Name = Devhost
Machine Type = 2 vCPUs (n-1standard-2 instance)
Identity and API Access = Allow full access to all Cloud APIs

All other settings left to default

![](https://github.com/zjserapin/distributed-project3/blob/master/images./Screen%20Shot%202020-04-16%20at%204.00.57%20PM.png)

Once your instance pops up, click on SSH to open your SSH window.

Step 2: Set up your environment and launch your build

Follow these commands/steps to install Scala, sbt and compile your code

![](https://github.com/zjserapin/distributed-project3/blob/master/images./Screen%20Shot%202020-04-16%20at%207.32.33%20PM.png)

After this, build out the feature dector files.  Your will clone in the Dataproc repository from github, cd into it in order to move forward 

Step 3: Run this command to build a "fat JAR" of the feature detector, allowing it to be submitted to Dataproc

sbt assembly

Step 4: Create a GCS bucket and add sample images

Name your buket, then use the gsutil program to create it.
Then you will use the curl command to place pictures in your bucket

![](https://github.com/zjserapin/distributed-project3/blob/master/images./Screen%20Shot%202020-04-16%20at%207.42.12%20PM.png)

Step 5: Create your cluster

set a cluster name to the MYCLUSTER variable.

![](https://github.com/zjserapin/distributed-project3/blob/master/images./Screen%20Shot%202020-04-16%20at%207.41.21%20PM.png)

Step 6: Submit the job to Cloud Dataproc and look at the results

![](https://github.com/zjserapin/distributed-project3/blob/master/images./Screen%20Shot%202020-04-16%20at%207.49.58%20PM.png)

Check storage browser to make sure you recieved the job.
Click the imgs folder and then navigate to the out/ folder to see where your results are stored.

![](https://github.com/zjserapin/distributed-project3/blob/master/images./Screen%20Shot%202020-04-16%20at%206.09.34%20PM.png)

We can see by the "before and after" pictures that the job was successful!

![](https://github.com/zjserapin/distributed-project3/blob/master/images./imgs_classroom.jpg)

#
![](https://github.com/zjserapin/distributed-project3/blob/master/images./out_classroom_output.jpg)

This completes the demo!

Check out this video for a more in depth look: 

