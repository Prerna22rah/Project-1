
pipeline {
 agent any
 stages{ 
  stage('clone code'){
   steps {git 'https://github.com/Prerna22rah/Project-1' }
}
  stage('Docker Build Image') {
   steps { sh 'docker build -t prinshu/project-1:1.0 .'}
    }
  }
}
