pipeline{
    agent{label 'docker'}
    stages {
        stage('vcs') {
            steps{
               git url : 'https://github.com/Jenkin-pipeline/StudentCoursesRestAPI.git',
                  branch : 'develop'              
                }
        } 
             stage('build') {
                steps {
                    sh 'docker image build -t shaikkhajaibrahim/spc:latest .'
                }
        }
         stage('scan and push') {
            steps {
                sh 'echo docker scan shaikkhajaibrahim/spc:latest'
            }
        }
    }
}