pipeline
{
    agent {
        lable 'slave-node'
    }
    stages
    {
        stage("info")
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
