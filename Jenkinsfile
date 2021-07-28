pipeline {

    agent any
    
    stages {

        stage('Git Branch') {

            steps {

                echo "$GIT_BRANCH"
                sh(script: 'echo Hello World')
                sh(script: 'date')
                sh(script:'ls -ll')
            }
        }
    }
}
