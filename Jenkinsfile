node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Checkout code from repository
   def scmVars = checkout scm
   def now = sh returnStdout: true, script: 'date | tr -d "\n"'
   
   // currentBuild.displayName = "#${BUILD_NUMBER} | ${BRANCH_NAME} | ${scmVars.GIT_COMMIT}"
   currentBuild.description = "Build #${BUILD_NUMBER}\n${now}\nBranch: ${BRANCH_NAME}\nCommit Hash: ${scmVars.GIT_COMMIT}"
   
   // Mark the code build 'stage'....
   stage 'Build'

   sh "cat README.md"
   sh "cat Jenkinsfile"
   
   echo "Branch Name: $BRANCH_NAME"
   sh "printenv"

   
}
