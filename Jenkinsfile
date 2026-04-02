pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/2025sl93064-SakshamMishra/labsheet1-2025sl93064.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "Building the project..."'
            }
        }
        stage('Test') {
            steps {
                sh '''
                python3 - <<EOF
import calculator
assert calculator.add(20,30) == 50
assert calculator.sub(50,20) == 30
print("Tests passed")
EOF
                '''
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deployment stage (will update later)"'
            }
        }
    }
}
