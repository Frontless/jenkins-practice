pipeline {
     agent any
     stages {
        stage("Build") {
            steps {
                sh "sudo npm install"
                sh "sudo npm run build"
            }
        }
        stage("Deploy") {
            steps {
                sh "sudo rm -rf /home/ubuntu/jenkins-practice"
                sh "sudo cp -r ${WORKSPACE}/build/ /home/ubuntu/jenkins-practice/"
            }
        }
    }
}
