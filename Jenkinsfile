Pipeline {
    Agent {
        Node {
            Label 'pipeline-practice'
        }
    }

     Triggers {
            PollSCM '*/5 * * * *'
     }

    Stages {
        Stage('build') {
            Steps {
                echo "building..."
                Sh 'echo "test build stage"'
            }
        }

        Stage('Test') {
            Steps {
//                 Checkout([
//                     $class: 'GitSCM',
//                     Branches: [[name: '*/master']],
//                     UserRemoteConfigs: [[url: 'https://github.com/spring-projects/spring-petclinic.git']]
//                 ])
                echo "test..."
                Sh 'echo "test Test stage"'
            }
        }

        Stage('Code Deliver') {
            Steps {
                   Sh 'echo "test deliver stage"'
//                 Sh 'mvn install -Dmaven.test.skip=true'
            }
        }
    }
}