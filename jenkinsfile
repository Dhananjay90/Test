pipeline {
    agent 
    {
        label "WINDOWS_NODE"
    }

    stages {
        stage('Git Checkout') {
            steps {
                echo 'Git Checkout'
                git credentialsId: '0db7b3f0-b56b-4f7b-9de3-b719d1c49a05', url: 'https://github.com/Dhananjay90/Test.git'
            }
        }
        
    stage('Run test.py') {
            steps {
                powershell "python test.py"
            }
        }
    stage('Run Add.py') {
            steps {
                powershell "python add.py"
            }
        }
    }
}
