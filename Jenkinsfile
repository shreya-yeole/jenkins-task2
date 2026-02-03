pipeline {
    agent any

    stages {
        stage('clone') {
            steps {
                git branch: 'main', url: 'https://github.com/shreya-yeole/jenkins-task2.git'
            }
        }

        stage('Run script') {
            steps {
                sh './hello.sh'

            }
        }
        stage('success') {
            steps {
                echo "script executed successfully"
            }
        }
    }
	post {
        success {
            echo "✅ Build, push, and deploy completed successfully!"
        }
        failure {
            echo "Pipeline failed. Check logs."
        }
    }
}
