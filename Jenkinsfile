
node {

    withMaven(maven:'maven') {

        stage('Checkout') {
            git url: 'https://github.com/yuvaraj09/Microservices.git'
        }

        stage('Build') {
            sh 'mvn clean install' 

            def pom = readMavenPom file:'pom.xml'
            print pom.version
            env.version = pom.version
        }

     
    }

}