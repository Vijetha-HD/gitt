pipeline
{
    agent any
    stages
    {
        stage('nginx image')
        {
            steps
            {
                sh 'docker pull nginx'
            }
        }
    stage('to stop container')
    {
        steps
        {
            sh 'docker stop app'
        }
    }
        stage('to remove'){
            steps{
                sh 'docker rm app'
            }
        }
        stage('to run'){
            steps{
                sh 'docker run -it -d --name app -p 80:80 nginx'
            }
        }
    }
}
