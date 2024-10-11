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

   NAME                 TYPE           CLUSTER-IP      EXTERNAL-IP                           PORT(S)                      AGE
kong-gateway-proxy   LoadBalancer   10.63.250.199   example.eu-west-1.elb.amazonaws.com   80:31929/TCP,443:31408/TCP   4m41s


