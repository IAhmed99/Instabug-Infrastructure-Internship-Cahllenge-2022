node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'docker-hub') {

        def dockerImage = docker.build("iahmed99/instabug-cahllenge")

        dockerImage.push()
    }
}