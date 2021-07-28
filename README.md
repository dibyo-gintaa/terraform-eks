# terraform-eks

kubectl create mindway-docker-secret docker-registry mindway-docker-secret \
--docker-server=https://index.docker.io/v2/ \
--docker-username=****** \
--docker-password=******* \
--docker-email=dibyojyoti.chatterjee@ivycomptech.com \
--namespace=default


kubectl create secret mindway-docker-secret docker-registry mindway docker-server=https://index.docker.io/v2/ docker-username=****** docker-password=****** docker-email=dibyojyoti.chatterjee@ivycomptech.com namespace=default


kubectl create secret docker-registry mindway-docker-secret --docker-server=https://index.docker.io/v2/ --docker-username=dibyoivy --docker-password=Dibyo@123 --docker-email=dibyojyoti.chatterjee@ivycomptech.com --namespace=default



kubectl port-forward analytics 80:8501

 kubectl port-forward analytics-69769cfdf9-hg5bx 5002:8501
 kubectl port-forward api-85f4c7f4fb-8wct4 5001:80
 
 

 
 curl -O https://releases.hashicorp.com/terraform/0.15.3/terraform_0.15.3_linux_amd64.zip
 
Check where to unzip package
Find out executable path
[root@localhost]# echo $PATH
/sbin:/bin:/usr/sbin:/usr/bin
unzip terraform_0.15.3_linux_amd64.zip -d /usr/bin/

eksctl create iamserviceaccount --cluster=mindway-mvp-develop --namespace=kube-system --name=aws-load-balancer-controller --attach-policy-arn=arn:aws:iam::607844630435:policy/AWSLoadBalancerControllerAdditionalIAMPolicy --override-existing-serviceaccounts --approve
helm upgrade -i aws-load-balancer-controller eks/aws-load-balancer-controller --set clusterName=mindway-mvp-develop --set serviceAccount.create=false --set serviceAccount.name=aws-load-balancer-controller -n kube-system

kubectl get deployment -n kube-system aws-load-balancer-controller

psql -h <host> -p <port> -d <master_db> -U <master_user>

psql -h  mindway.cmqayhhzggr1.eu-west-2.rds.amazonaws.com -p 5432 -d mindway -U postgres

EMPTY_TABLES_SECRET: "delete-is-okay"
SPECIAL_POSTGRES_READ: "1"


k8s-default-apiingre-dbeeff81f2-976959355.eu-west-2.elb.amazonaws.com/docs/empty_all_tables/delete-is-okay

kubectl replace --force -f analytics-deployment.yaml




