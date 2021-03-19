// @Image(cloudbees/codeship-jenkinsfile-step:nodejs)
pipeline {
  agent any
  stages {
    stage('Web Tests') {
      stages {
        stage('Nodejs Setup') {
          steps {
            sh """
              npm i -S express pug
              node ./hello.js &
            """
          }   
        }
      }  
    }
    stage('Build and Push Image') {
      when {
        beforeAgent true
        branch 'master'
      }
      steps {
        checkout scm
        echo "TODO - build and push image"
      }
    }
  }
}
