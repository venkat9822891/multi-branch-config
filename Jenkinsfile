node('slv1') {
   stage('Cont.Downloads') 
     {
     git 'https://github.com/venkat9822891/multi-branch-config.git'
      }
   stage('Cont.Builds') 
     {
    sh 'mvn package'
     }
  stage('Cont.Deployments') 
    {
    deploy adapters: [tomcat8(credentialsId: '7b795a2c-b95e-4f27-885a-165270d3b598', path: '', url: 'http://172.31.44.40:8080')], contextPath: '/prod-app', war: '**/*.war'
    }
}
