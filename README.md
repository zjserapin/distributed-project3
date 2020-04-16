# UNCC DSBA 6190 Assignment 3: Cloud Map Reduce and Distributed Jobs

Task Use a distributed computing platform and perform a task suited to the platform. You can demo one of the reference labs or you can implement a custom project (say word count on Spark on AWS EMR).
#
For this assignment I decided to demo the Google qwicklab Distributed Image Processing in Cloud Dataproc

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

1[](https://github.com/zjserapin/distributed-project3/blob/master/images./Screen%20Shot%202020-04-16%20at%207.32.33%20PM.png)

After this, build out the feature dector files.  Your will clone in the Dataproc repository from github, cd into it in order to move forward 




