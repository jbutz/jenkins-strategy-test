node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Checkout code from repository
   def scmVars = checkout scm
   def now = sh returnStdout: true, script: 'date | tr -d "\n"'
   
   // currentBuild.displayName = "#${BUILD_NUMBER} | ${BRANCH_NAME} | ${scmVars.GIT_COMMIT}"
   currentBuild.description = "Build #${BUILD_NUMBER}<br />${now}<br />Branch: ${BRANCH_NAME}<br />Commit Hash: ${scmVars.GIT_COMMIT}<br />Version: ???<br />EC2 Instance: ???"
   
   // Mark the code build 'stage'....
   stage 'Build'

   sh "cat README.md"
   sh "cat Jenkinsfile"
   
   echo "Branch Name: $BRANCH_NAME"
   sh "printenv"

   
}
