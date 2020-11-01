pipeline {
    agent any

    environment {
        HOSTNAME = "${sh(script:'echo $HOSTNAME', returnStdout: true).trim()}"
    }

    stages {
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('Docker Build') {
          steps{
            echo "${env.HOSTNAME}"
            sh(script: "which docker")
            sh(script: "which java")
            // sh(script: 'docker images -a')
            // sh(script: """
            //   cd azure-vote/
            //   docker images -a
            //   docker build -t jenkins-pipeline .
            //   cd ..
            // """)
          }
        }
    }
}
