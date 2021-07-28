 pipeline {

    agent any

    stages {

        stage('Git Branch') {

            steps {

                echo "$GIT_BRANCH"
                sh(script: 'echo Hello World')
                sh(script: 'date')
                sh(script:'ls -ll')
                sh(script:'hostname')
            }
        }
        stage('Docker Build') {

            steps {
                sh(script: 'sudo su')
                sh(script:"""
                  cd azure-vote/
                  /usr/local/bin/docker docker images -a 
                  docker build -t jenkins-pipeline .
                  docker images -a
                  cd ..
                """)
            }
        }
    }
}
