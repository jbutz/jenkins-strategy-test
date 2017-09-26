node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Checkout code from repository
   checkout scm

   // Mark the code build 'stage'....
   stage 'Build'

   sh "cat README.md"
   sh "cat Jenkinsfile"
   
   echo "Branch Name: $BRANCH_NAME"

   sh "printenv"
}
