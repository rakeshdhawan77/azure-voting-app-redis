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
                sh(script: 'docker images -a')
                sh(script:"""
                  cd azure-vote/
                  docker images -a
                  docker build -t jenkins-pipeline .
                  docker images -a
                  cd ..
                """)
            }
        }
    }
}
