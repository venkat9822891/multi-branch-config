node{
   stage('Cont.Downloads') 
     {
     git branch: 'dev', url: 'https://github.com/venkat9822891/multi-branch-config.git'
      }
   stage('Cont.Builds') 
     {
    sh 'mvn package'
     }
  stage('Cont.Deployments') 
    {
    deploy adapters: [tomcat8(credentialsId: 'ce8c6d56-0d5f-4813-8543-552debf338ac', path: '', url: 'http://172.31.43.36:8080')], contextPath: '/dev-app', war: '**/*.war'
    }
}
