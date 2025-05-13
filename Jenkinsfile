// This pipeline is triggered via Jenkins SCM Polling (not webhook).

pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Task: Compile and package the source code.'
                echo 'Tool: Maven'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit and integration tests to ensure functional and component-level correctness.'
                echo 'Tool: JUnit'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Task: Perform static code analysis to enforce coding standards and detect issues.'
                echo 'Tool: SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Task: Scan code for known vulnerabilities in dependencies and source code.'
                echo 'Tool: OWASP Dependency-Check'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the built application to a staging environment (AWS EC2 instance).'
                echo 'Tool: AWS CLI'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Perform integration and acceptance tests in a staging environment.'
                echo 'Tool: Selenium'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy the tested and verified application to the production environment (AWS EC2 instance).'
                echo 'Tool: AWS CLI / Ansible'
            }
        }
    }
}
