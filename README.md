I just want to build a HPE Ezmeral Container Platform to play with the various Data Management capabilities e.g. Backup/Restore, Disaster Recovery and Application Mobility. It is challenging to create a HPE ECP cluster if you are not familiar to it. After the ECP Cluster is up running, we still need to install Kasten, create a sample DB, create policies etc.. The whole process is not that simple.

![image](https://f.hubspotusercontent30.net/hub/3855032/hubfs/Blog-featured-image-HPE%20Ezmeral-Kasten%20K10.png?width=720&name=Blog-featured-image-HPE%20Ezmeral-Kasten%20K10.png)

This script based automation allows you to build a ready-to-use Kasten K10 demo environment on a running HPE Ezmeral Container Platform on AWS Cloud. If you don't have a HPE ECP Cluster, you can follow the guide from the link. Once the ECP Cluster is up running, you can proceed to the next steps. 

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/KUlH2o405oI/0.jpg)](https://www.youtube.com/watch?v=KUlH2o405oI)

# Here're the prerequisities. 
1. Log in to the terminal which you can access the ECP Cluster via Kubectl
2. Clone the github repo to your local host, run below command
````
git clone https://github.com/yongkanghe/ecp-k10.git
````
3. Complete the preparation tasks first
````
cd ecp-k10;./hpeprep.sh
````
4. Optionally, you can customize region, bucketname, object storage profile etc.
````
vim setenv.sh
````
 
# To build the labs, run 
````
./k10-deploy.sh
````
1. Install Kasten K10
2. Deploy a Postgresql database
3. Create an IBM COS location profile
4. Create a backup policy
5. Run an on-demand backup job

## NOTE: IBM Cloud Shell is emphemeral. 

The cloned respository including the temporary files will be removed after no activity for one hour. If that happened, you need to run below steps to re-created the files before you can destroy the labs. 

## To create the repository and the temporary files
````
git clone https://github.com/yongkanghe/ecp-k10.git;cd ecp-k10;./hpeprep.sh
````

# To delete the labs, run 
````
./k10-destroy.sh
````
1. Remove Postgresql Database
2. Remove Kasten K10
3. Remove all the relevant disks
4. Remove all the relevant snapshots
5. Remove the objects from the bucket

# Learn how to backup/restore containers on ECP Cluster
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/zMKIOCuEPyI/0.jpg)](https://www.youtube.com/watch?v=zMKIOCuEPyI)

# For more details about HPE Ezmeral Backup and Restore
https://blog.kasten.io/protect-cloud-native-applications-on-hpe-ezmeral-with-kasten-k10

# Kasten - No. 1 Kubernetes Backup
https://kasten.io 

# Kasten - DevOps tool of the month July 2021
http://k10.yongkang.cloud

# Contributors

### [Yongkang He](http://yongkang.cloud)
### [Adrian Gigante](https://www.linkedin.com/in/ron-xing-hua/)



