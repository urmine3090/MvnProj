pipeline {
  agent {
    node {
      label 'Akshay'
    }

  }
  stages {
    stage('Sub') {
      parallel {
        stage('Sub') {
          steps {
            git(url: 'https://github.com/urmine3090/MvnProj.git', changelog: true, branch: 'Basic')
          }
        }

        stage('Sub_2') {
          steps {
            container(name: 'Basic_2', shell: 'test') {
              timestamps() {
                echo 'Hello'
              }

            }

          }
        }

      }
    }

  }
  environment {
    Akshay = '10'
  }
}