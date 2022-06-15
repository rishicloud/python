pipeline 
{
agent { label 'built-in' }
stages
{
stage('clone from git')
{
steps
{
git branch: 'master', url: 'https://github.com/bravatjammu/python.git'
}
}

stage('test')
{
steps
{
sh "pytest"
sh(""" /jenkins/workspace/""")
}
}
stage('test wtih flake8')
{
steps
{
sh "flake8 ."
}
}  
}
}