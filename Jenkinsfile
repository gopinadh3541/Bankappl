node('master') {
   stage('Checkout')
    {
        git 'https://github.com/gopinadh3541/Bankappl.git'
    }
    stage('Clean')
    {
        bat 'mvn clean test'
    }
   stage('Proceed to Packaging?')
    {
       input 'Proceed to Packaging?'
    }
   
    stage('Packaging')
    {
        bat 'mvn install'
    }
    
    /*stage('Deploy')
    {
        
     parallel firstBranch: {
       build job: 'New_appl', parameters: [string(name: 'DEPLOYMENT_ARTIFACT_PATH', value: 'C:\\jenkins_installpath\\workspace\\BankAppl\\target'), string(name: 'DEPLOYMENT_ARTIFACT_NAME', value: 'BankExample')]
    }, secondBranch: {
        build job: 'Tomcat_appl', parameters: [string(name: 'DEPLOYMENT_ARTIFACT_PATH', value: 'C:\\jenkins_installpath\\workspace\\BankAppl\\target'), string(name: 'DEPLOYMENT_ARTIFACT_NAME', value: 'BankExample')]
    },
    failFast: true
    
    }*/
    
}

    
 
