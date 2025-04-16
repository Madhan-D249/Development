pipeline
{
  agent any
    stages
    {
      stage('info')
      {
        steps{
        sh ''' echo${env.JOB_NAME}
        echo${env.BUILD_ID}
        pwd
        uptime
        hostname
        '''
      }
    }
}
}
