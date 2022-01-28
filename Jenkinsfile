 pipeline{

     agent any

     stages{
        
        stage('Checking out codigo base'){
            steps{
                checkout scm: [$class: 'GitSCM',userRemoteConfigs:[[credentialsId: 'mi-llave-ssh-github', url: 'git@github.com:jvinc86/maven-project-hello-world.git']]]
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