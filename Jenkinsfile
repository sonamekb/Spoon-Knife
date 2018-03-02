pipeline {
  agent any
  stages {
    stage('build') {
      parallel {
        stage('build') {
          steps {
            echo 'Implementing stage1'
            readFile 'index.html'
          }
        }
        stage('build2') {
          steps {
            writeFile(file: 'webtext.html', text: '"Hello"')
          }
        }
      }
    }
    stage('test') {
      steps {
        readFile 'index.html'
      }
    }
  }
}