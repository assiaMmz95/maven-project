pipeline {

agent any
stages {
stage('init') {
steps{
bat 'C://apache-maven-3.9.12//bin//mvn clean '
archiveArtifacts 'target/*.jar'
}
}
stage('test') {
steps{
bat 'C://apache-maven-3.9.12//bin//mvn test '
archiveArtifacts 'target/*.jar'
junit 'target/surefire-reports/*.xml'
}
}
stage('build') {
steps{
bat 'C://apache-maven-3.9.12//bin//mvn package'
archiveArtifacts 'target/*.jar'
}
}
}
}