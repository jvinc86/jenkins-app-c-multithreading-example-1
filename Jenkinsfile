 pipeline{

     agent any

     stages{
        
        stage('Checking out codigo base'){
            steps{
                checkout scm: [$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[credentialsId: 'mi-llave-ssh-github', url: 'https://github.com/jvinc86/jenkins-app-c-multithreading-example-1']]]
            }
        }

        stage('Build'){
            steps{
                sh 'gcc mt-example-0.c -lpthread'
            }
        }

        stage('Test'){
            steps{
                sh './a.out'
            }
        }

        stage('Deploy'){
            steps{
                sh 'echo Done'
            }
        }
     }
 }