pipeline {
    agent {
        docker {
            image 'babibe2211/jenkin_php'
        }
    }
    stages {
        stage('Prepare') {
            steps {
                sh "hostname"
                //sh 'rm -rf *'
                //sh 'git clone https://github.com/pmbibe/Docker'
                //sh "chmod -R 755 Docker"
            }
        }
        stage('Test') {
            steps {
                echo "--------------------Test Stage---------------------"
                sh "chmod +x *"
                sh "ant"
            }
        }
        stage('Deploy') {
            steps {
                echo "--------------------Deploy Stage---------------------"
                junit 'build/logs/*.xml'
                //sh "Jenkins_Dockerfile/Deploy.sh"
            }
        }
    }
}
