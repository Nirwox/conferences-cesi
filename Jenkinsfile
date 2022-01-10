pipeline {
    agent any

    stages {
        stage('Copy source') {
            steps {
                sh 'git clone "https://github.com/Nirwox/1treize3.git"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mv /var/lib/jenkins/workspace/CI_conferencescesi_FRONT_APP/ /home/admin/conferencescesi/'
            }
        }
    }
}