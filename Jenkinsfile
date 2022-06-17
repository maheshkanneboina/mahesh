node('master')
{
    stage('Continuous Download')
        {

    git 'https://github.com/sunildevops77/maven.git'
        }
    stage('Continuous Build')
        {
    sh label: '', script: 'mvn package'
        }
    stage('Continuous Deployment')
        {
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/mahesh_loan/webapp/target/webapp.war   ubuntu@172.31.8.124:/var/lib/tomcat9/webapps/qaenv.war'
        }
    stage('Continuous Testing')
        {
              sh label: '', script: 'echo "Testing Passed"'
        }
    stage('Continuous Delivery')
        {
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/mahesh_loan/webapp/target/webapp.war   ubuntu@172.31.9.40:/var/lib/tomcat9/webapps/prodenv.war'
        }
}


