node {
    stage('Build') {
        steps {
            sh 'npm install'
        }
    }

    stage('Test') {
        steps {
            sh 'npm test'
        }
    }

    stage('Containerization') {
        steps {
            script {
                docker.build("your-docker-image-name:latest")
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}

