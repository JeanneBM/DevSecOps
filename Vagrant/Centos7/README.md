## Useful commands:
```
docker run
docker stop; docker rm
docker build
docker create 
docker ps
docker images
docker container ls
docker volume ls

sudo docker-compose up -d
whereis git
netstat -tnlp
chmod +x docker_env.sh //no such a command as script ./

//sudo: docker-compose: command not found//
sudo curl -L https://github.com/docker/compose/releases/download/1.21.0/docker-compose-$(uname -s)-$(uname -m) -o /usr/local/bin/docker-compose; sudo chmod +x /usr/local/bin/docker-compose; sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose

```

## Init
```
vagrant init centos/7
vagrant up
vagrant ssh

vagrant ssh-config >> C:/Users/ ... /.ssh/config

# /usr/bin/ssh init@127.0.0.1 -p 2222

sudo yum upgrade; sudo yum install -y vim; sudo yum install -y net-tools; sudo yum install -y wget; ssh-keygen; yum install -y git; yum install -y maven; 
```

## Static IP
https://www.itzgeek.com/how-tos/linux/centos-how-tos/how-to-configure-static-ip-address-in-centos-7-rhel-7-fedora-26.html


## Partition
```
lsblk; df -h
fdisk /dev/sda 
```
## Docker CE on CentOS:
```
sudo yum install -y yum-utils; sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo; sudo yum install -y docker-ce docker-ce-cli containerd.io; yum list docker-ce --showduplicates | sort -r; sudo yum install -y docker-ce-<VERSION_STRING> docker-ce-cli-<VERSION_STRING> containerd.io; sudo systemctl start docker; sudo docker run hello-world
docker version
sudo groupadd docker; sudo usermod -aG docker $USER; sudo reboot ; [after reboot] sudo systemctl start docker; sudo systemctl status docker
```
## Jenkins:
```
sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo; sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key; sudo yum upgrade; sudo yum install -y epel-release java-11-openjdk-devel; sudo yum install -y jenkins; sudo systemctl daemon-reload; sudo systemctl start jenkins; sudo systemctl enable jenkins; sudo systemctl status jenkins


```

## Git
```
git add .; git commit -m "Final"; git remote add origin https:// ... .git
git push -u origin master

vim Dockerfile
docker build -t git .
```

## Docker_env
```
docker run --name tomcat -it --rm -p 8888:8080 -d tomcat
docker run --name sonar -it --rm -p 9000:9000 -d sonarqube
docker run --name nexus -it --rm -p 8081:8081 -d sonatype/nexus3
docker run --name selenium_hub -it --rm -p 4441:4441 -d selenium/hub:4.1.0-20211209
docker run --name selenium_node_firefox -it --rm -p 4442:4442 -d selenium/standalone-firefox:4.1.0-20211209
docker run --name selenium_node_chrom -it --rm -p 4444:4444 -d selenium/standalone-chrome:4.1.0-20211209
docker run --name Jenkins -it --rm  -p 8080:8080 -p 50000:50000 -d -v /c/Users/.../app/jenkins:/var/jenkins_home jenkins/jenkins
```
