#!/usr/bin/env groovy

import com.tikalk

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
            notifyBuild('SUCCESS', 'sample.html')
        }
        failure {
            notifyBuild('FAILURE', 'sample.html')
        }  
        unstable {
            notifyBuild('UNSTABLE', 'sample.html')
        }            
    }
}
