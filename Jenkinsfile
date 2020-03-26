node {
    stage('Git checkout') {
        git branch:'master', url:'https://github.com/atinsingh/pipe2.git'
    }
    stage('Execute Script') {
        sh 'chmod +x script.sh'
        sh 'sh script.sh'
    }
    stage('Notify via Email') {
        emailext body: 'BUILD IS GOOD', subject: 'BUILD PASS', to: 'atin@pragra.co'
    }
}
