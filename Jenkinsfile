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
#                  /usr/local/bin/docker 'docker images'
#                  docker images ls 
                  /usr/local/bin/docker images
                  /usr/local/bin/docker build -t jenkins-pipeline .
                  /usr/local/bin/docker images
                  cd ..
                """)
            }
        }
    }
}
