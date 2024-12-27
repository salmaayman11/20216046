pipeline {
    agent any
    tools {
        git 'Default' // Matches the name set in Git installations
    }
    stages {
        stage('Clone Repository') { 
            steps {
                git url: 'https://github.com/salmaayman11/20216046', branch: 'main'
            }
        }
        stage('Execute Script') { 
            steps {
                script {
                    if (isUnix()) {
                        // On Unix-like OS (Linux/macOS), use sh to execute the script
                        sh './script.sh'
                    } else {
                        // On Windows, use Git Bash (bash.exe) to run the script
                        // Ensure that the full path to bash.exe is correct, or Git Bash is in PATH
                        bat '"C:\\Program Files\\Git\\bin\\bash.exe" script.sh'
                    }
                }
            }
        }
    }
}