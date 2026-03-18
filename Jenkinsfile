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
                sh("./mvnw clean compile test-compile")
                echo("Build completed.")
            }
        }
        stage("Test"){
            steps {
                echo("Running tests...")
                sh("./mvnw test")
                echo("Tests completed.")
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