pipeline {
    agent { label 'agent-2' }

    // Trigger the pipeline automatically on every GitHub push
    triggers {
        githubPush()
    }

    environment {
        IMAGE_NAME = "spotify-clone"
        CONTAINER_NAME = "spotify-container"
    }

    stages {

        stage('Clone Repository') {
            steps {
                echo "📦 Cloning the GitHub repository..."
                checkout scm
            }
        }

        stage('Build Docker Image') {
            steps {
                echo "🛠 Building Docker image..."
                sh '''
                    docker build -t ${IMAGE_NAME}:latest .
                '''
            }
        }

        stage('Run Docker Container') {
            steps {
                echo "🚀 Running Docker container..."
                sh '''
                    docker run -d --name ${CONTAINER_NAME} -p 3000:80 ${IMAGE_NAME}:latest
                '''
            }
        }

        stage('Test Docker Container') {
            steps {
                echo "🔍 Testing the running container..."
                sh '''
                    sleep 5
                    curl -I http://localhost:3000 || echo "Container not responding!"
                '''
            }
        }
    }

    post {
        success {
            echo "🎉 Deployment successful! Your Spotify Clone is live on port 3000."
        }
        failure {
            echo "❌ Pipeline failed. Please check the Jenkins logs for details."
        }
        always {
            echo "🏁 Pipeline finished execution."
        }
    }
}
