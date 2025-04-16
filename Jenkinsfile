pipeline
{
    agent {
        label 'slave-node'
    }
    tools
    {
        maven 'maven'
    }
    stages
    {
        stage("build")
        {
            steps{
                mvn 'clean package'
            }
        }
    }
}
