node('master') {
   stage('download') {
   git 'https://github.com/priyankagirhe15/febmulti.git'
}
 stage('Build') {
   sh 'mvn package'
} 
 stage('deploy') {
  sh 'scp /home/ubuntu/.jenkins/workspace/multipipe_loans/webapp/target/webapp.war ubuntu@172.31.33.13:/var/lib/tomcat8/webapps/qaenv.war'
} 
 stage('test') {
   sh 'echo "tested"'
} 
 stage('delivery') {
  sh 'scp /home/ubuntu/.jenkins/workspace/multipipe_loans/webapp/target/webapp.war ubuntu@172.31.41.73:/var/lib/tomcat8/webapps/prodenv.war'
} 

}
