pipeline {
  agent any
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            build 'build'
            echo 'Building'
          }
        }

        stage('') {
          steps {
            sh '''Jenkins/build

pipeline
agent any 
{
stages{
stage{echo "build"}'''
          }
        }

      }
    }

    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing'
            junit(allowEmptyResults: true, healthScaleFactor: 1, testResults: 'ok')
          }
        }

        stage('Test Normal') {
          steps {
            sh '''Jenkins/test




pipeline
agent any 
{
stages{
stage{echo "test"}'''
            echo 'normal test'
          }
        }

        stage('Integration testing') {
          steps {
            sh '''Jenkins/integration testing




pipeline
agent any 
{
stages{
stage{echo "integration testing"}'''
          }
        }

        stage('Archive tests') {
          steps {
            junit 'Above normal'
            sh '''Jenkins/Archive tests




pipeline
agent any 
{
stages{
stage{echo "Archive tests"}'''
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'Deploy'
        sh '''Jenkins/Deploy




pipeline
agent any 
{
stages{
when branch master
stage{echo "Deploy"}'''
      }
    }

  }
}