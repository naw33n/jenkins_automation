[6:41 PM] Nisha Raut
pipeline {

    agent any
 
    stages {

        stage('Code fetch') {

            steps {

                echo 'Code Fetch from github'

                git url :'https://github.com/nisharaut388/jenkins1.git', branch: 'main'

            }

        }

        stage('Build') {

            steps {

                sh 'docker build -t my-new-website .'
 
            }

        }

        stage('Deploy') {

            steps {

                echo 'Deploy on Container'

                sh 'docker run -t -p 80:80 my-new-website '

            }

        }

    }

}

