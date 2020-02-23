## artifactory


# Installation

JDK 1.8
sudo yum install java-1.8.0-openjdk-devel

Installing Artifactory
wget https://bintray.com/jfrog/artifactory-rpms/rpm -O bintray-jfrog-artifactory-rpms.repo
sudo mv bintray-jfrog-artifactory-rpms.repo /etc/yum.repos.d/
sudo yum install jfrog-artifactory-oss


# Update the Java options and the artifactory related path

vi artifactory.default  and update the Xms value to 1g

export JAVA_OPTIONS="-server -Xms512m -Xmx1g…. 
export ARTIFACTORY_HOME=/var/opt/jfrog/artifactory

# Running Artifactory
To start or stop Artifactory you must be running as root and can use the following command:
            cd /opt/jfrog/artifactory/bin$service artifactory start | stop

# Setup Service
sudo service artifactory start













