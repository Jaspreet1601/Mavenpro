pipeline{     agent any 
    tools { 
        maven 'm1' 
    } 
    stages 
    { 
        stage("checkout") 
        {             steps{ 
                git branch: 'master', url: 'https://github.com/Jaspreet1601/Mavenpro.git' 
            } 
        } 
        stage("clean_01") 
        {             steps{ 
                bat 'mvn clean' 
            } 
        } 
        stage("validate_02") 
        {             steps{ 
                bat 'mvn validate' 
            } 
        } 
 
        stage("compile_03") 
        {             steps{                 bat 'mvn compile' 
            } 
        } 
        stage("test_04") 
        {             steps{                 bat 'mvn test' 
            } 
        } 
        stage("package_05") 
        {             steps{                 bat 'mvn package' 
            } 
        } 
        stage("intergration-test_06") 
        {             steps{                 bat 'mvn integration-test' 
            } 
        } 
        stage("verify_07") 
        {             steps{ 
                bat 'mvn verify' 
            } 
        } 
        stage("install_08") 
        {             steps{ 
                bat 'mvn install' 
            } 
        } 
        stage("deploy_09") 
        { 
            steps{ 
                bat 'mvn deploy : deploy file' 
            } 
        } 
    } } 
