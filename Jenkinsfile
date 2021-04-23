pipeline{
    agent any

    stages{
        stage('Verify Branch') {
            steps {
                npm pack
                npm start
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
