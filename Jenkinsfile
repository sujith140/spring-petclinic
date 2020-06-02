node
{
stage('svn')
{
git branch: 'master', url: 'https://github.com/sujith140/spring-petclinic.git'
}
stage('package')
{
sh 'mvn package'
}
stage('archiev')
{
archiveArtifacts 'target/*.jar'
}
stage('results')
{
junit 'target/surefire-reports/*.xml'
}
}
