pipeline {
    agent any

    stages {
        stage('Clone Source') {
            steps {
                catchError {
                    sh 'git clone "https://github.com/Nirwox/1treize3.git"'
                }
            }
        }
        stage('Clean') {
            steps {
                    sh 'rm -rf /home/admin/conferencescesi/CI_conferencescesi_FRONT_APP/'
            }
        }
        stage('Clean useless file') {
            steps {
                    sh 'rm -rf /var/lib/jenkins/workspace/CI_conferencescesi_FRONT_APP/.git'
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp -R -T /var/lib/jenkins/workspace/CI_conferencescesi_FRONT_APP/ /home/admin/conferencescesi/'
            }
        }
    }
}