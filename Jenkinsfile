
# change your respective GITHUB folder url
#change the path of python folder(python.exe) according to your local system (In cmd type where python)

pipeline {
    agent any

    environment {
        VENV = "venv"
    }

    stages {
        stage('Clone GitHub Repo') {
            steps {
                git branch: 'main', credentialsId: 'https://github.com/vasudev152/Pipelining_pythonApp.git', url: 'https://github.com/your-username/Pipelining_pythonApp.git'
            }
        }

        stage('Set Up Python Virtual Environment') {
            steps {
                bat '"C:\\Users\\your-username\\AppData\\Local\\Programs\\Python\\Python310\\python.exe" -m venv venv'
                bat '.\\venv\\Scripts\\python.exe -m pip install --upgrade pip'
                bat '.\\venv\\Scripts\\pip install flask pandas numpy tensorflow' 
            }
        }

        stage('Run Flask App') {
            steps {
                bat '.\\venv\\Scripts\\python app.py'
            }
        }
    }
}
