pipeline {
   agent any

   stages {
      stage('Verify Branch') {
         steps {
            echo "$GIT_BRANCH"
         }
      }
      stage('Example') {
        try {
         sh 'exit 1'
        }
        catch (exc) {
         echo 'Something failed, I should sound the klaxons!'
         throw
        }
      }
   }
}
