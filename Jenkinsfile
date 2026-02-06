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
        	mail bcc: '', body: 'The commit from the github for task2 has been triggered.', cc: '', from: '', replyTo: '', subject: 'Commit from github TRiggered', to: 'Yeoleshreya08@gmail.com'

		}
	}
}
