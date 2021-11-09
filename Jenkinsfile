pipeline {

    // Disable ConcurrentBuilds
    options { disableConcurrentBuilds() }

    environment {
        TAG_NAME = "${env.BRANCH_NAME}"
    }

    agent any// Change to your own team's node

    stages {
        stage("dev-step0") {
            steps {
                sh 'echo dev-step0'
            }
        }

        stage("test-step0") {

            steps {
                sh 'echo test-step0'
            }
        }
        stage("dev-step1") {
            when {
                branch "dev"
            }
            steps {
                sh 'echo dev-step1'
            }
        }
         stage("test-step1") {
            when {
                branch "test"
            }
            steps {
                sh 'echo test-step1'
            }
        }
    }
}
