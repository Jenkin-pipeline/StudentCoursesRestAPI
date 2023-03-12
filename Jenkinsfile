pioeline{
    agent{label 'docker'}
    stages {
        stage('vcs') {
            steps{
               git url : 'https://github.com/Jenkin-pipeline/StudentCoursesRestAPI.git',
                  branch : 'staging'              
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