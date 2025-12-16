pipeline {
    agent any

    triggers {
        pollSCM('*/5 * * * *')
    }

    stages {
        stage('Dev') {
            steps {
                echo "Building..."

                withMaven(
                            maven: 'maven-3',
                            // Use `$WORKSPACE/.repository` for local repository folder to avoid shared repositories
                            mavenLocalRepo: '.repository',
                            mavenSettingsConfig: 'my-maven-settings'
                        ) {
                          sh "mvn clean verify"
                        }
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
