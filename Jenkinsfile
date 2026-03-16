pipeline {
    agent {
        node {
            label "linux && java21"
        }
    }
    stages {
        stage("Build"){
            steps {
                echo("Building the project...")
            }
        }
        stage("Test"){
            steps {
                echo("Running tests...")
            }
        }
         stage("Deploy"){
            steps {
                echo("Deploying the application...")
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