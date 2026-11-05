pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building application...'
                bat '"C:/Users/Ashutosh Singh/AppData/Local/Programs/Python/Python311/python.exe" -m py_compile app.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing application...'
                bat '"C:/Users/Ashutosh Singh/AppData/Local/Programs/Python/Python311/python.exe" app.py'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                bat 'if not exist deployment mkdir deployment'
                bat 'copy app.py deployment\\app.py'
            }
        }
    }

    post {
        success {
            echo 'CI/CD pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Check the console output.'
        }
    }
}
