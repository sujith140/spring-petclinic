node
{
stage('svn')
{
git branch: 'sprint1', url: 'https://github.com/sujith140/spring-petclinic.git'
}
stage('package')
{
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
}
