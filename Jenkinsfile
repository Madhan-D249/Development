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
                sh""" echo ${env.BUILD_ID}
                echo ${env.JOB_NAME}
                pwd
                uptime
                hostname
                """
            }
        }
    }
}
