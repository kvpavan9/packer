node {
  stage('git checkout'){
    git credentialsId: 'github', url: 'https://github.com/kvpavan9/packer.git'
  }
  stage('Maven Build'){
    def mvnHome=tool name: 'mvn', type: 'maven'
    def mvnCMD ="${mvnHOME}/bin/mvn"
    sh "${mvnCMD} clean package"
  }
}
