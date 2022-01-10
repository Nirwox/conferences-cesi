pipeline {
    agent any

    stages {
        stage('Copy source') {
            steps {
                sh 'wget https://github.com/Nirwox/1treize3/archive/refs/heads/master.zip'
            }
        }
        stage('Deploy') {
            steps {
                sh 'mv /var/lib/jenkins/workspace/CI_conferencescesi_FRONT_APP/ /home/admin/conferencescesi/'
            }
        }
    }
}