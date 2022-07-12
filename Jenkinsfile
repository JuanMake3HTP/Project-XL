pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "Esto es el build"
                echo "agrego otra linea"
            }
        }
        stage('Scan') { 
            steps {
                withSonarQubeEnv('sonarqube'){
                    sh 'mvn sonar:sonar -Dsonar.login=8f4f794e071c5e937b98024a451bec3a646162d5' 
                }
            }
        }
        stage('Test') { 
            steps {
                echo "Este es el test"
            }
        }
        stage('Deploy') { 
            steps {
                echo "Este es el deploy"
            }
        }
    }
}
