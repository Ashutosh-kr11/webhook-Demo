pipeline {
    agent any

    triggers {
        // This listens to GitHub webhooks
        githubPush()
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                echo "✅ Build triggered by GitHub Webhook!"
                sh 'echo "Code commit hash: $(git rev-parse HEAD)"'
            }
        }
        stage('Test') {
            steps {
                echo "🧪 Running Tests..."
                sh 'echo "Pretend tests passed ✅"'
            }
        }
        stage('Deploy') {
            steps {
                echo "🚀 Deploy step triggered (Demo Only)"
            }
        }
    }
}
