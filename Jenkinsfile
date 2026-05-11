pipeline {
    agent any  // Use any available agent
    
    environment {
        LANG = 'en_US.UTF-8'
        LC_ALL = 'en_US.UTF-8'
    }   // this has to be added only if you get an error saying UTF required is 8 but showing in ISO00009

    tools {
        maven 'Maven'  // Ensure this matches the name configured in Jenkins
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Checkout Stage'
                //git branch: 'main', url: 'https://github.com/jynx0405/MavenAnsibleWebApp1.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build Stage'
                //sh 'mvn clean package'
            }
        }

        stage('Archive') {
            steps {
                echo 'Archive Stage'
                //archiveArtifacts artifacts: 'target/*.war', fingerprint:true
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy Stage'
                //sh 'mvn clean package'
                //sh 'ansible-playbook ansible/playbook.yml -i ansible/hosts.ini'
            }
        }
    }
}
