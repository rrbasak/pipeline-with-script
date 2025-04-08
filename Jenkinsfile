pipeline{
    agent any
    stages{
        stage('compile') {
            steps {
                bat 'javac Test.java'
            }
        }
        stage('run') {
            steps {
                bat 'java Test'
            }
        }
    }
    post{
        always{
            bat 'echo "This will always run"'
        }
        success{
            bat 'echo "Build Succeeded"'
        }
        failure{
            bat 'echo "Build Failed"'
        }
    }
}