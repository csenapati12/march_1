node(){
    stage("checkout"){
        echo "Inside Checkout"
        checkout changelog: false, poll: false, scm: [$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/csenapati12/java-tomcat-maven-docker.git']]]
    }
     stage("mvn build"){
        echo "Maven build"
        bat label: '', script: 'mvn package'
        
    }
     stage("Sonar analysis"){
        echo "Sonar Analysis"
    }
     stage("Nexus Upload"){
        echo "Nexus Upload"
    }
     stage("Docker build"){
        echo "Docker Build"
    }
     stage("Docker Run"){
        echo "Docker Run"
    }
}
