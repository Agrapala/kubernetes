🚀 Kubernetes RBAC Explained in Simple Terms

When multiple teams share a Kubernetes cluster, not everyone should have admin access. That's where RBAC (Role-Based Access Control) helps.

🔐 RBAC controls: • Who can access the cluster
 • What resources they can access
 • What actions they can perform

✅ Authentication = Who are you? (AD, LDAP, Keycloak, etc.)
 ✅ Authorization = What can you do? (RBAC)

Key Components

👤 User → Human identity

🤖 ServiceAccount → Identity for applications running in Kubernetes

📋 Role → Defines permissions within a namespace

🔗 RoleBinding → Assigns a Role to a User, Group, or ServiceAccount

🌐 ClusterRole → Cluster-wide permissions

🔗 ClusterRoleBinding → Grants ClusterRole access across the cluster

Real-World Example

👨‍💻 Developer: View Pods & Deployments
 🧪 Tester: View Pods & Logs
 ⚙️ DevOps: Manage Deployments & Services

RBAC ensures everyone gets only the permissions they need, following the Principle of Least Privilege.

Useful Commands
Shell
kubectl auth can-i get pods -n dev
kubectl auth can-i delete pods --as=john -n dev
kubectl get roles -n dev
kubectl get rolebindings -n dev

🎯 Takeaway: Kubernetes security isn't just about deploying workloads. Understanding RBAC is essential for securing clusters, protecting production environments, and implementing least-privilege access.

#Kubernetes #RBAC #DevOps #KubernetesSecurity #DevSecOps #CloudNative #CKA #CKAD