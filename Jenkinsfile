pipeline {
    agent any

    stages {
        stage('Copy source') {
            steps {
                catchError {
                    sh 'git clone "https://github.com/Nirwox/1treize3.git"'
                }
            }
        }
        stage('Deploy') {
            steps {
                sh 'cp -R /var/lib/jenkins/workspace/CI_conferencescesi_FRONT_APP /home/admin/conferencescesi/'
            }
        }
    }
}