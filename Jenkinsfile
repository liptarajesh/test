pipeline {
    agent any
    stages {
        stage('build somefiles') {
            steps {
                sh 'mvn install'
                sh 'sudo cp -r /root/.m2/repository/com/mycompany/app/my-app/1.jar /root/'
            }
        }i
	  stage('Deploy') {
             steps {
                sh 'sudo docker build -t sureshimage2 .'
                sh 'sudo docker container run -itd --name mycontainer sureshimage2:latest'
            }
        }

     }
 }
