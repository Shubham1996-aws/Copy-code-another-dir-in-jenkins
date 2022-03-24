pipeline {
    agent any

    stages {
        stage('Git Clone') {
            steps {
                git branch: 'main', url: 'https://github.com/Shubham1996-aws/vuejs.git'
            }
        }
        
        stage('Copy code to Dir') {
            steps {
                sh "cp -r $JENKINS_HOME/workspace/job /home/ubuntu/pipeline"
            }
        }
        
        stage('Run Script') {
            steps {
                sh "cd /home/ubuntu/pipeline/job && chmod 777 script.sh && ./script.sh"
            }
        }
    }
}
