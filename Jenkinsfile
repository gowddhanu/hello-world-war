pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                 sh 'rm -rf hello-world-war'
                 sh 'git clone https://github.com/gowddhanu/hello-world-war.git' 
            }
        }
        stage('Test') { 
            steps {
                sh 'mvn -f /var/lib/jenkins/workspace/declarativeScript/hello-world-war/pom.xml package'
                //sh 'mvn package'
            }
        }
        stage('Deploy') { 
            steps {
                echo "this is deploy stage" 
            }
        }
    }
}