pipeline {
    agent {label "agent"}

    stages {
        stage('Code') {
            steps {
                echo "This is cloning the Code"
                git url:"https://github.com/khobaibkhan117/django-notes-app.git", branch:"main"
                echo "Clone Successfull"
            }
        }
        stage('Build') {
            steps {
                echo "This is building the Code"
                sh "docker build -t notes-app:latest ."
            }
        }
        stage('Test') {
            steps {
                echo "This is testing Code"
            }
        }
        stage('Deploy') {
            steps {
                echo "This is deploying the Code"
                sh "docker run -d -p 8000:8000 notes-app:latest"
            }
        }
    }
}
