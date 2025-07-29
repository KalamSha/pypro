pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Checking Python syntax...'
                bat 'python -m py_compile helo.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'python -m unittest discover -s tests'
            }
        }

        stage('Run') {
            steps {
                echo 'Running your Python script...'
                bat 'python helo.py'
            }
        }
    }
}
