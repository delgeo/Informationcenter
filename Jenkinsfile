pipeline {
	agent {docker { image 'pooja1989/maven:v1.1' }}
    stages {
         stage('Build') {
		              
            steps {
		withDockerContainer('pooja1989/maven_sonar') {
                 git credentialsId: 'GitHub', url: 'https://github.com/poojasree/InformationCentre.git'
                sh 'mvn clean install sonar:sonar'
                }               
            }
        } 
         
    }
}
