node {
 stage('SCM Checkout'){
  git 'https://github.com/pradippokharkar/mavensample'
}
stage('Compile-Package'){
def mvnHOME=tool name: 'Maven1', type: 'maven'
 sh "${mvnHOME}/bin/mvn package"
}
}
