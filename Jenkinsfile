node {
   def mvnHome
      stage('checkout') { 
      git credentialsId: 'MyID', url: 'https://github.com/rita19872/hello-world2.git'

      mvnHome = tool name: 'M2', type: 'maven'
      env.JAVA_HOME = tool 'JDK1.8'
                         }
   stage('Build') 
   {
     if (isUnix())
     {
         sh "'${mvnHome}/bin/mvn' clean install"
     } else {
           bat(/"${mvnHome}\bin\mvn" clean install/)
            }       
       
   }
   }
  
   