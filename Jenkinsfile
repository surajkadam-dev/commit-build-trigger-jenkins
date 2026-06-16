pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/surajkadam-dev/commit-build-trigger-jenkins.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Building Application...'
                sh 'python --version'
            }
        }

        stage('Test') {
            steps {
                echo 'Running Tests...'
                sh 'python -m unittest'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }
}