node {
 stage('SCM Checkout'){
  git 'https://github.com/pradippokharkar/mavensample'
}
stage('Compile-Package'){
def mvnHOME=tool name: 'Maven1', type: 'maven'
 sh "${mvnHOME}/bin/mvn package"
}
 stage('deploytotomcat'){

sshagent(('tomcat-dev')){

sh 'scp -o StrictHostKeyChecking=no target/*.war ec2-user@172.31.21.229:/opt/tomcat/webapp'
}
}
}
