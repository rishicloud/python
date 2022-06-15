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
stage('installing dependencies')
{
steps
{
sh "pip install flake8"
sh "pip install pytest"
sh "python3 -m pip install --upgrade pip setuptools wheel"
sh "pip install -r requirements.txt"
sh "pip install pytest-cov"
}
}
stage('test')
{
steps
{
sh "pytest"
}
}
stage('test wtih flake')
{
steps
{
sh "flake8 ."
}
}  
}
}