pipeline{
  agent any

  stages{

    stage('Checkout'){
      steps{
        echo 'Fetching source code'
        checkout scm
      }
    }

    stage('Code Quality CHeck!'){
      steps{
        echo 'Checking code quality'
        bat '''
        findstr GOOD quality.txt > nul
        if errorlevel 1(
          echo Code Quality Failed
          exit 1
        ) else (
            echo Code Quality Passed
        ) '''
      }
    }
    
  }
}
