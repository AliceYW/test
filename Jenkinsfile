pipeline {
  agent none
  stages {
    stage('aa') {
      parallel {
        stage('master_stage_1') {
          steps {
            node(label: 'master') {
              sh '''echo master
hostname -I'''
            }
            
          }
        }
        stage('slave_stage_1') {
          steps {
            node(label: 'ubuntu') {
              sh '''echo slave:
hostname -I'''
            }
            
          }
        }
      }
    }
  }
}