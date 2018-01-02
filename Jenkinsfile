#!groovy
node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'

   // Get some code from a GitHub repository
   checkout scm
   def grdlHome = tool 'gradle4'

   // Mark the code build 'stage'....
   stage 'Build'
   sh "${grdlHome}/bin/gradle build"
   
   stage 'Test'
   sh "${grdlHome}/bin/gradle test"
}
