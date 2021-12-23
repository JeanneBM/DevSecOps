Docker CE on CentOS:

sudo yum install -y yum-utils; sudo yum-config-manager --add-repo https://download.docker.com/linux/centos/docker-ce.repo; sudo yum install docker-ce docker-ce-cli containerd.io; yum list docker-ce --showduplicates | sort -r; sudo yum install docker-ce-<VERSION_STRING> docker-ce-cli-<VERSION_STRING> containerd.io; sudo systemctl start docker; sudo docker run hello-world

Jenkins:

sudo yum install wget; sudo wget -O /etc/yum.repos.d/jenkins.repo https://pkg.jenkins.io/redhat-stable/jenkins.repo; sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key; sudo yum upgrade; sudo yum install epel-release java-11-openjdk-devel; sudo yum install jenkins; sudo systemctl daemon-reload