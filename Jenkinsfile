node {

    checkout scm

    docker.withRegistry('https://registry.hub.docker.com', 'docker-hub') {

        def customImage = docker.build("iahmed99/golang-task")

        customImage.push()
    }
}