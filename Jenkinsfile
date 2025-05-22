pipeline {
    agent any
    stages {
        stage('拉取代码') {
            steps {
                git branch: 'main', url: 'https://github.com/soongzx/maven-project.git'
            }
        }
        stage('编译项目') {
            steps {
                sh 'mvn clean install'
            }
        }
        stage('运行测试') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
