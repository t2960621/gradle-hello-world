#!groovy
node('master') {
   // Mark the code checkout 'stage'....
   stage ('Checkout'){

      // Get some code from a GitHub repository
      checkout scm
      
   }

   // Mark the code build 'stage'....
   stage ('Build Gradle'){
      // Get the maven tool.
      // ** NOTE: This 'maven3' maven tool must be configured
      // **       in the global configuration.
      def grdHome = tool 'gradle4'
      // Run the maven build
     // sh "${grdHome}/bin/gradle clean install"
     //sh 'gradle build'
      
     sh "${grdHome}/bin/gradle build --info"
   }
}



//Runs on node ‘slave1’
//•Has a stage checkout - to get code from git
//•Has a stage ‘build’ executing ‘gradle build’
