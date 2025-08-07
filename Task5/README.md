Последовательно действий для запуска

1. Запустить Minikube

2. Создать поды запустив команды:

   kubectl run front-end-app --image=nginx --labels role=front-end --expose --port 80
   kubectl run back-end-app --image=nginx --labels="roel=back-end-api" --expose --port 80 
   kubectl run admin-front-end-app --image=nginx --labels="role=admin-front-end" --expose --port 80 
   kubectl run admin-back-end-app --image=nginx --labels="role=admin-back-end-api" --expose --port 80

3. Настроить сетевые политики выполнив команду:

   kubectl apply -f non-admin-api-allow.yaml
