pipeline {
  agent any
  tools {
    nodejs '24.1.0'
  }

  options {
    timeout(time: 2, unit: 'MINUTES')
  }

  stages {
    stage('Install dependencies') {
      steps {
        
		powershell 'Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force; npm install' 
      }
    }
    stage('Run tests') {
      steps {
        powershell 'Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass -Force; npm test'

      }
    }
  }
}
