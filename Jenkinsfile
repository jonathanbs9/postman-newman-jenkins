node {
    stage('Postman tests'){
        git 'https://github.com/jonathanbs9/postman-newman-jenkins.git'
        sh 'npm install'
        try {
            sh 'npm run test-api'
            currentBuild.result= 'SUCCESS'
        } catch (Exception ex) {
            currentBuild.result= "FAILURE"
        }
        junit 'newman_report.xml'
    }
}
