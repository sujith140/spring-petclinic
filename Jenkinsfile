node
{
stage('svn')
{
git 'https://github.com/sujith140/spring-petclinic.git'
}
stage('package')
{
if(env.BRANCH_NAME=='master'){
sh 'mvn package'
}
else{
sh 'mvn clean package'
}
}
stage('archiev')
{
archiveArtifacts 'target/*.jar'
}
stage('results')
{
junit 'target/surefire-reports/*.xml'
}
stage('echo')
{
if(env.BRANCH_NAME=='sprint1')
{
echo 'successfully completed execution'
}
else
{
echo 'something is fishy'
}
}
}