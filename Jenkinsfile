#!/usr/bin/env groovy

@Library('tikal-advanced-pipeline@master') _

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
                sh "echo '''$(pwd)'''"
            }
        }
    }
    post {
        success {
            echo "===================== 1.0 ========================"
            TAP_email('SUCCESS','sample.html')
            echo "===================== 2.0 ========================"
        }
        failure {
            TAP_email('FAILURE','sample.html')
        }  
        unstable {
            TAP_email('UNSTABLE','sample.html')
        }            
    }
}
