pipeline {
    agent any

    stages {
        stage('Clone Source') {
            steps {
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                    sh 'git clone "https://github.com/Nirwox/1treize3.git"'
                }
            }
        }
        stage('Clean') {
            steps {
                    sh 'rm -rf /home/admin/conferencescesi/CI_conferencescesi_FRONT_APP/'
            }
        }
        stage('Delete .git folder') {
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