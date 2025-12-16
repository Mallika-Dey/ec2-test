pipeline {
    agent any
    
    triggers {
        pollSCM('*/5 * * * *')
    }

    stages {
        stage('Dev') {
            steps {
                echo "Building..."

                sh ''
                sh 'echo "Test build stage"'
            }
        }

        stage('Test') {
            steps {
                echo "Testing..."
                sh 'echo "Test Test stage"'
            }
        }

        stage('Code Deliver') {
            steps {
                sh 'echo "Test deliver stage"'
                // sh 'mvn install -Dmaven.test.skip=true'
            }
        }
    }
}
