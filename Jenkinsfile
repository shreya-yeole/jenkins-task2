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
    always {
        emailext(
            body: "Commit triggered this build. Check console output.",
            to: "yeoleshreya08@gmail.com")
		}
	}
}
