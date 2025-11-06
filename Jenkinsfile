pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/dhavalsinhpatil/TestingCiCD.git'
            }
        }

        stage('Run Tests') {
            steps {
                echo 'Running QA test scripts...'
                bat 'python test_script.py'
            }
        }

        stage('Post Results') {
            steps {
                echo '✅ All tests executed successfully'
            }
        }
    }
}
