pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/dhavalsinhpatil/TestingCiCD.git'
            }
        }

        stage('Compile Java Code') {
            steps {
                echo 'Compiling Java test file...'
                bat 'javac TestSuite.java'
            }
        }

        stage('Run Tests') {
            steps {
                echo 'Running QA test scripts...'
                bat 'java TestSuite'
            }
        }

        stage('Post Results') {
            steps {
                echo '✅ All tests executed successfully'
            }
        }
    }
}
