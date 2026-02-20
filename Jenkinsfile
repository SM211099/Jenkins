pipeline {
    agent any

    stages {
        stage("Build") {
            steps {
                echo "Hello World"
            }
        }

        stage("Test") {
            steps {
                echo "mkdir Shubham"
            }
        }

        stage("Deploy") {
            steps {
                echo "touch Shubham.txt"
            }
        }
    }

    post {
        success {
            mail to: 'mangalwedhekarshubham75073@gmail.comm',
                 subject: "Build SUCCESS: ${env.JOB_NAME}",
                 body: "Build completed successfully."
        }

        failure {
            mail to: 'mangalwedhekarshubham75073@gmail.com',
                 subject: "Build FAILED: ${env.JOB_NAME}",
                 body: "Build failed. Please check Jenkins."
        }
    }
}
