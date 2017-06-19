#!/usr/bin/env groovy

@Library("tikal-advanced-pipeline") _

pipeline 
{
    agent any
    stages 
    {
        stage('Code Update') 
        {
            steps 
            {
                echo "===================== 0.0 ========================"
                sh "echo \$(pwd)"
            }
        }
    }
    post {
        success {
            echo "===================== 1.0 ========================"
            sh "echo \$(pwd)"
            sh "ls -la \$(pwd)/sample.html"            
            TAP_email('SUCCESS','sample.html')
            echo "===================== 2.0 ========================"
            deleteDir()
        }
        failure {
            TAP_email('FAILURE','sample.html')
            deleteDir()            
        }  
        unstable {
            TAP_email('UNSTABLE','sample.html')
            deleteDir()            
        }            
    }
}
