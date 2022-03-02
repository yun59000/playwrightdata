pipeline {
   agent { docker { image 'mcr.microsoft.com/playwright:focal' } }
   environment {
        HOME = '.'
    }
   stages {
       stage('install playwright') {
         steps {
            sh 'npm install -D @playwright/test'
            sh 'npx playwright install'
         }
      }
      stage('e2e-tests') {
         steps {
            sh 'npx playwright test'
         }
      }
   }
}
