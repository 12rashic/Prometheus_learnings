<h1> 🌵Getting started with Prometheus </h1>

![Static Badge](https://img.shields.io/badge/Prometheus-green) is one of the most trending tools used for monitoring of applications hosted on Kubernetes (k8s) , as its better in maintaining and monitoring of multiple servers / applications .
Also extending the functionality for "Alerting Mechanism" when working in integration with cloud native platforms like 

![Static Badge](https://img.shields.io/badge/AWS-pink)![Static Badge](https://img.shields.io/badge/Azure-blue)
![Static Badge](https://img.shields.io/badge/GCP-red)

<br> </br>

<h2> 💬 Pre-requisites </h2>
  <ol>📜 Minikube Installed </ol> 
  <ol>📜 Kubectl Installed </ol>
  <ol>🖱 Port 9090 Open </ol>
   
<h2> 🔌 Installation on Windows </h2>
  <ol> <strong>⚡OS : Windows (64-bit)</ol> </strong>
  <ol> <strong>⚡Package Manager used : Helm  </strong> </ol>

  <h2><strong> Step 1 </strong> <h1></h1>
    
            helm repo add prometheus-community https://prometheus-community.github.io/helm-charts
            helm repo update
            
  <br> </br>

  
  ![ScreenShot](https://github.com/12rashic/Prometheus_learnings/blob/main/helm_01.png})

  <h2><strong> Step 2 </strong> <h1></h1>

            helm install <Release-name> prometheus-community/prometheus 
  
            
  ![ScreenShot](https://github.com/12rashic/Prometheus_learnings/blob/main/helm_02.png})   

   <h2><strong> Step 3 </strong> <h1></h1>

            kubectl get po
            kubectl get svc

   ![ScreenShot](https://github.com/12rashic/Prometheus_learnings/blob/main/helm_03.png})  

       kubectl expose service prometheus-server --type=NodePort --target-port=9090 --name=prometheus-server-ext
       minikube service prometheus-server-ext

   follow the IP  that might appear on the screen / navigate to the <h3><kbd> IP Address :Port </kbd></h3> mentioned.

   ![ScreenShot](https://github.com/12rashic/Prometheus_learnings/blob/main/prometheusdashboard.png})  
  
            
  

  

  
  






  

