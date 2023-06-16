# First steps with Kubernets, Pods and Kind

## Step 1 - Create your Pod file
- Create a file with the name you want. In this example I'll be using `pod.yaml` to identify my Pod.
- Create your configuration:
```
apiVersion: v1
kind: Pod                                 # Defines the type 
metadata:
    name: nginx                           # This field is used to identify your Pod when you list them by typing `kubectl get pod`
    labels:
        name: nginx                       
spec:
    containers:
        - name: nginx
          image: nginx:latest
          ports:
              - containerPort: 80

```
