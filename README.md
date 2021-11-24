I just want to build a HPE Ezmeral Container Platform to learn the various Data Management capabilities e.g. Backup/Restore, Disaster Recovery and Application Mobility. It is challenging to create a HPE ECP cluster if you are not familiar to it. After the ECP Cluster is up running, we still need to install Kasten, create a sample DB, create policies etc.. The whole process is not that simple.

![image](https://camo.githubusercontent.com/d5e96661da3c02b0511af345f2c509e33567a09160d37d0df21c4e1e96b89d91/68747470733a2f2f662e68756273706f7475736572636f6e74656e7433302e6e65742f6875622f333835353033322f68756266732f426c6f672d66656174757265642d696d6167652d485045253230457a6d6572616c2d4b617374656e2532304b31302e706e673f77696474683d373230266e616d653d426c6f672d66656174757265642d696d6167652d485045253230457a6d6572616c2d4b617374656e2532304b31302e706e67)

This script based automation allows you to build a ready-to-use Kasten K10 demo environment on a running HPE Ezmeral Container Platform on AWS Cloud. If you don't have a HPE ECP Cluster, you can watch the Youtube video below. Once the ECP Cluster is up running, you can proceed to the next steps. 

[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/KUlH2o405oI/0.jpg)](https://www.youtube.com/watch?v=KUlH2o405oI)

# Here're the prerequisities. 
1. Log in to the terminal where you can access the ECP Cluster via Kubectl
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
3. Create a AWS S3 location profile
4. Create a backup policy
5. Run an on-demand backup job

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

# HPE ECP Backup and Restore
https://blog.kasten.io/protect-cloud-native-applications-on-hpe-ezmeral-with-kasten-k10

# Kasten - No. 1 Kubernetes Backup
https://kasten.io 

# Free Kubernetes Learning
https://learning.kasten.io 

# Kasten - DevOps tool of the month July 2021
http://k10.yongkang.cloud

# Contributors

### [Yongkang He](http://yongkang.cloud)
### [Ron Xing](https://www.linkedin.com/in/ron-xing-hua/)



