pipeline{
  agent any
  stages{
    stage("clone the repo"){
      steps{
        git url: "https://github.com/subhodeepGlobussoft/django-todo-cicd.git",branch: 'main'
      }
    }
    stage("build the dockerfile here"){
      steps{
        sh 'docker-compose down && docker-compose up -d'
      }
    }
  }
}
