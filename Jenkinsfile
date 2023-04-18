pipeline
{
  agent any
  stages
  {
    stage("clone the repo")
    {
      steps
      {
        git url: "https://github.com/subhodeepGlobussoft/django-todo-cicd.git",branch: 'develop'
      }
    }
    stage("build the dockerfile here")
    {
      steps
      {
        sh 'docker build -t django-todo'
      }
    }
    stage("run the image on port 8000")
    {
      steps
      {
        sh 'docker run -d -p 8000:8000 django-todo'
      }
    }
}
