pipeline {
    agent {
        node {
            label "linux && java21"
        }
    }
    stages {
        stage("Hello"){
            steps {
                echo("Hello Pipeline!")
            }
        }
    }

    post {
        always {
            echo("Pipeline finished.")
        }
        success {
            echo("Pipeline succeeded.")
        }
        failure {
            echo("Pipeline failed.")
        }
        cleanup {
            echo("Cleaning up resources.")
        }
    }
}