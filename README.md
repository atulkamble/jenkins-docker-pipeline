1) Task: Create jenkins pipeline | run Docker Image | command run 

1. Create Pipeline
2. Paste Jenkins Code in script
3. Build Now


// Console Output
```

```

2) Task: Create jenkins pipeline | run Docker Image | via github repo | command run 


Prerequisites: Tools: git 

Create Repo on github  - https://github.com/atulkamble/jenkins-docker-pipeline

Jenkinsfile << paste code | scripted pipeline code

Copy URL repo 

1) Create pipeline | git credentials
2) Description
3) SCM | git 
4) git config --global user.name "atulkamble"
git config --global user.email "atul_kamble@hotmail.com"
git config --list
5) Upload Jenkinsfile to your github repo
Create Public repo
>> Create Jenkinsfile >> add code
git add .
git commit -m "code"
git push origin main

6) copy url 
example: https://github.com/atulkamble/jenkins-docker-pipeline 
7) Create pipeline 
Update Github details, update branch details, select git credentials
8) Build Now

// Console Output
```
Started by user Atul Kamble
Obtained Jenkinsfile from git https://github.com/atulkamble/jenkins-docker-pipeline
[Pipeline] Start of Pipeline
[Pipeline] node
Running on Jenkins in /var/lib/jenkins/workspace/jenkins-docker-pipeline
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
Selected Git installation does not exist. Using Default
The recommended git tool is: NONE
using credential 2840aca2-7249-475f-8da3-9af7689d1a2c
Cloning the remote Git repository
Cloning repository https://github.com/atulkamble/jenkins-docker-pipeline
 > git init /var/lib/jenkins/workspace/jenkins-docker-pipeline # timeout=10
Fetching upstream changes from https://github.com/atulkamble/jenkins-docker-pipeline
 > git --version # timeout=10
 > git --version # 'git version 2.40.1'
using GIT_ASKPASS to set credentials 
 > git fetch --tags --force --progress -- https://github.com/atulkamble/jenkins-docker-pipeline +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git config remote.origin.url https://github.com/atulkamble/jenkins-docker-pipeline # timeout=10
 > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
Avoid second fetch
 > git rev-parse refs/remotes/origin/main^{commit} # timeout=10
Checking out Revision 7dffc7a268f22bacc0d9726e7f3fb5c1847f7131 (refs/remotes/origin/main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 7dffc7a268f22bacc0d9726e7f3fb5c1847f7131 # timeout=10
Commit message: "update"
First time build. Skipping changelog.
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] isUnix
[Pipeline] withEnv
[Pipeline] {
[Pipeline] sh
+ docker inspect -f . node:20.16.0-alpine3.20
.
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] withDockerContainer
Jenkins does not seem to be running inside a container
$ docker run -t -d -u 992:992 -w /var/lib/jenkins/workspace/jenkins-docker-pipeline -v /var/lib/jenkins/workspace/jenkins-docker-pipeline:/var/lib/jenkins/workspace/jenkins-docker-pipeline:rw,z -v /var/lib/jenkins/workspace/jenkins-docker-pipeline@tmp:/var/lib/jenkins/workspace/jenkins-docker-pipeline@tmp:rw,z -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** node:20.16.0-alpine3.20 cat
$ docker top 963c26129e0dd2dc16b6caa3e12d772031a564918cf4505d410e42bda824a95d -eo pid,comm
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Test)
[Pipeline] sh
+ node --version
v20.16.0
[Pipeline] }
[Pipeline] // stage
[Pipeline] }
$ docker stop --time=1 963c26129e0dd2dc16b6caa3e12d772031a564918cf4505d410e42bda824a95d
$ docker rm -f --volumes 963c26129e0dd2dc16b6caa3e12d772031a564918cf4505d410e42bda824a95d
[Pipeline] // withDockerContainer
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // node
[Pipeline] End of Pipeline
Finished: SUCCESS```





