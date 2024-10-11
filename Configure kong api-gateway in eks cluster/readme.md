Deploy the Kong Ingress Controller

1. Add the Kong Helm repo

   helm repo add kong https://charts.konghq.com
   helm repo update

2. Deploy the Kong Ingress Controller using Helm:

    helm install kong kong/ingress -n kong --create-namespace

The results should look like this:

NAME: kong
LAST DEPLOYED: Tue Oct  3 15:12:38 2023
NAMESPACE: kong
STATUS: deployed
REVISION: 1
TEST SUITE: None

3. Get the IP address at which Kong is accessible:

   kubectl get services -n kong

   The results should look like this:

 <img width="390" alt="image" src="https://github.com/user-attachments/assets/0ff49da7-e1ce-40f0-a62f-850a9772704c">



