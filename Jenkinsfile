pipeline {
    agent { label 'centos' } // Указываем, что этот пайплайн должен запускаться на агенте с меткой 'centos'
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                git url: 'https://github.com/polskeysh/jenkins1', branch: 'master' // Или master
            }
        }
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Пример для Maven:
                // sh 'mvn clean install'
                // Пример для Python:
                sh 'ls -la' // Просто листинг файлов для проверки
                sh 'echo "Build complete on Jenkins Agent!"'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'echo "Tests passed (simulated)." '
            }
        }
    }
}
