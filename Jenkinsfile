node
{
stage('svn')
{
git url: 'https://github.com/sujith140/spring-petclinic.git'
}
stage('package')
{
if(env.branch=='master'){
sh 'mvn package'
}
else{
sh 'mvn clean package'
}
stage('archiev')
{
archiveArtifacts 'target/*.jar'
}
stage('results')
{
junit 'target/surefire-reports/*.xml'
}
if(env.branch=='sprint1')
{
echo 'successfully completed execution'
}
}
