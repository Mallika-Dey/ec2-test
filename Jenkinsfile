pipeline {
    agent {
        node {
            label 'pipeline-practice'
        }
    }
    
    triggers {
        pollSCM('*/5 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo "Building..."
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
