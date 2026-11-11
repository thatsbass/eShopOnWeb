pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'dotnet build eShopOnWeb.slnx'
      }
    }

    stage('Test') {
      steps {
        sh 'dotnet test tests/UnitTests'
      }
    }

    stage('Deployment') {
      steps {
        sh 'dotnet publish src/Web/Web.csproj -c Release -o ./publish'
      }
    }

  }
}