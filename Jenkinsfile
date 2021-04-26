pipeline{
    agent any

    stages{
        stage('start application') {
            steps {
                npm pack
                npm start
            }
            stage('Checkout') {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/imnitin28/node-hello.git']]])
            }
            post {
                success {
                    echo "App started succesfully"
                }
                failure {
                    echo "Some error ocurred"
                }
            }
        }
    }
}
