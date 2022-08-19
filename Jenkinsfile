pipeline
{
    agent any
    stages
    {
        stage('Continous Download_saving')
        {
            steps
            {
                git ' https://github.com/AnilGitSpace/TomcatCode.git'
            }
        }
        stage('Continous Build_saving')
        {
            steps
            {
               sh 'mvn package' 
            }
        }
        stage('Continous Dpeloyment_saving')
        {
            steps
            {
             sh 'sshpass -p "ubuntu" scp /home/ubuntu/.jenkins/workspace/scripted-pipeline/target/flipkart.war ubuntu@172.31.13.179:/home/ubuntu/apache-tomcat-9.0.65/webapps/'
            }
            
        }
    }
}
