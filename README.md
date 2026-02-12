# Flask-Aug25
creating web-api using flask

# Uploade Docker images to ECR
1- ECR repo - flask_loan_repo
2- aws ecr get-login-password --region eu-north-1 | docker login --username AWS --password-stdin 285633211459.dkr.ecr.eu-north-1.amazonaws.com
3- docker build -t flask_loan_repo .
4- docker tag flask_loan_repo:latest 285633211459.dkr.ecr.eu-north-1.amazonaws.com/flask_loan_repo:latest
5- docker push 285633211459.dkr.ecr.eu-north-1.amazonaws.com/flask_loan_repo:latest

# Create Cluster in ECS
1- Cluster Name : loan_app_cluster
2- Task definitions - loan_app_task
3- Run Servie Name- loan_app_service
4- go to task - Download task-defination in JSON and put it on Repo
5- container-name: loan_app_container

# .githib/Workflows/autmate.yml

1- region: eu-north-1
2- repo name: flask_loan_repo
3- clusterName: loan_app_cluster
4- Run Servie Name- loan_app_service
5- container-name: loan_app_container

# Secret and Variables

Settings-Secret Varaibles-> [secret]-> New Repo. Secret-> AWS_ACCESS_KEY_ID : AKFIDFDAUFAIQ5RBWCIDFDF
Settings-Secret Varaibles-> [secret]-> New Repo. Secret-> AWS_SECRET_ACCESS_KEY:nquO4vxhgfgfmxBGxa1vmLkbSfdshsfdtjhgf
