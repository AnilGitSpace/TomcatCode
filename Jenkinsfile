pipeline
{
    agent any
    stages
    {
        stage('Continous Download')
        {
            steps
            {
                git ' https://github.com/AnilGitSpace/TomcatCode.git'
            }
        }
        stage('Continous Build')
        {
            steps
            {
               sh 'mvn package' 
            }
        }
        stage('Continous Dpeloyment')
        {
            steps
            {
             sh 'sshpass -p "ubuntu" scp /home/ubuntu/.jenkins/workspace/scripted-pipeline/target/flipkart.war ubuntu@172.31.13.179:/home/ubuntu/apache-tomcat-9.0.65/webapps/'
            }
            
        }
    }
}
