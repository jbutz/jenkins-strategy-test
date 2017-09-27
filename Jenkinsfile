node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Checkout code from repository
   def scmVars = checkout scm
   
   echo "$scmVars"
   
   currentBuild.displayName = "#${BUILD_NUMBER} | ${BRANCH_NAME} | ${scmVars.GIT_COMMIT}"
   
   // Mark the code build 'stage'....
   stage 'Build'

   sh "cat README.md"
   sh "cat Jenkinsfile"
   
   echo "Branch Name: $BRANCH_NAME"
   sh "printenv"

   
}
