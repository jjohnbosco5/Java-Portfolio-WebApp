node
{
def mavenHome = tool name: "maven4.0.0"
    
    stage("1. git clone")
    {
       git url: 'https://github.com/LandmakTechnology/maven-web-app.git'
    }
    
    stage("2. Build")
    {
        sh "${mavenHome}/bin/mvn clean package"

        // bat "mvn clean package"  - for winows OS
    }
    stage('3. Sonar')
    {
         //sh "${mavenHome}/bin/mvn sonar:sonar"
    }
    stage('4. Nexus')
     {
        // sh "${mavenHome}/bin/mvn deploy"
    }
    stage('5. Deploy')
    {
       //sh "scp -o StrictHostKeyChecking=no target/maven-web-app ec2-user@34.204.166.28:/opt/apache-tomcat-9.0.37/webapps/"
        
    }
    stage('6. Email notification')
    {
        //
    }
}

