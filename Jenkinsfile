pipeline {
    agent {
        node{
            label 'AGENT-1'
        }
    }
    environment { 
        greetings = "Hi I am learning jenkins pipeline"
    }

    stages {
        stage('Build') {
            steps {
                sh """
                    echo "Here I am writing shell script"
                    env "$greetings"
                """
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'Script is failed'
        }
        success { 
            echo 'Hey Script is success!'
        }
    }
}

