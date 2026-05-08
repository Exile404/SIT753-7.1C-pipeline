pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build stage: Compile the source code and package the application into deployable artefacts.'
                echo 'Tool: Maven (build automation tool for Java projects).'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Unit and Integration Tests stage: Run unit tests to verify individual components and integration tests to verify components work together correctly.'
                echo 'Tools: JUnit for unit testing and Selenium for automated integration testing.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Code Analysis stage: Statically analyse the source code for quality issues, code smells, and adherence to industry coding standards.'
                echo 'Tool: SonarQube (static code analysis platform).'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Security Scan stage: Scan source code and project dependencies to identify known vulnerabilities and CVEs.'
                echo 'Tool: OWASP Dependency-Check (security vulnerability scanner).'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploy to Staging stage: Deploy the built artefact to a staging server that mirrors production configuration.'
                echo 'Tool: AWS CLI deploying to an AWS EC2 staging instance.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Integration Tests on Staging stage: Run end-to-end integration tests against the staging environment to validate behaviour in a production-like setup.'
                echo 'Tool: Postman / Newman for automated API integration testing on the staging server.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploy to Production stage: Promote the validated artefact to the production environment for end users.'
                echo 'Tool: AWS CodeDeploy targeting an AWS EC2 production instance.'
            }
        }
    }
}
