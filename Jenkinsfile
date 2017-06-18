#!/usr/bin/env groovy

@Library('tikal-advanced-pipeline@master') _

import com.tikalk.utils

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
            }
        }
    }
    post {
        success {
            utils(notifyBuild('SUCCESS', 'sample.html'))
        }
        failure {
            utils(notifyBuild('FAILURE', 'sample.html'))
        }  
        unstable {
            utils(notifyBuild('UNSTABLE', 'sample.html'))
        }            
    }
}
