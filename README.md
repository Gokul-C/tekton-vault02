# tekton Clone-Build-StaticAnalysis-ImageBuilding
# Optional -  Pre requisite
```
https://github.com/Gokul-C/tekton-workspaces
```
# 1. Setup sonarqube server as docker container
```
docker run -d -p 9000:9000 sonarqube
```
After docker container is up -
  1. Open sonarqube UI: IP:9000
  2. Default credentials: admin admin
  3. Create new project
  4. save that project token
These details are necessary to push our code to sonarqube

# 2. Create pv-pvc 
```
https://raw.githubusercontent.com/Gokul-C/tekton-sonarqube/main/pv-pvc.yaml
```

# 3. Create tasks
```
https://raw.githubusercontent.com/Gokul-C/tekton-sonarqube/main/tasks.yaml
```
# 4. Create pipeline
```
https://raw.githubusercontent.com/Gokul-C/tekton-sonarqube/main/pipeline.yaml
```
# 5. Create pipelinerun
```
https://raw.githubusercontent.com/Gokul-C/tekton-sonarqube/main/pipelinerun.yaml
```
# Expected output:
<img width="960" alt="Screenshot 2024-01-15 211127" src="https://github.com/Gokul-C/tekton-sonarqube/assets/46756853/311b3dd5-bf7c-4cf0-b9fc-c08288efa4d0">
<img width="743" alt="Screenshot 2024-01-15 211357" src="https://github.com/Gokul-C/tekton-sonarqube/assets/46756853/b17ebd84-11ac-4cea-bff3-df808e69557d">
<img width="959" alt="Screenshot 2024-01-15 211423" src="https://github.com/Gokul-C/tekton-sonarqube/assets/46756853/128fccf7-d037-46ff-8239-0f2745ba24a4">
<img width="744" alt="Screenshot 2024-01-15 211459" src="https://github.com/Gokul-C/tekton-sonarqube/assets/46756853/11bbef81-8116-498d-b425-d5ffba8ad5e7">
<img width="948" alt="Screenshot 2024-01-15 211522" src="https://github.com/Gokul-C/tekton-sonarqube/assets/46756853/73643b09-4e79-44d0-939d-bc99e6760b23">





