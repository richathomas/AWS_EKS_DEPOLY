## AWS EKS
### Understanding Kubernetes Fundamentals
#### EKS vs. Self-Managed Kubernetes: Pros and Cons
Managed Control Plane: EKS takes care of managing the Kubernetes control plane components, such as the API server, controller manager, and etcd. AWS handles upgrades, patches, and ensures high availability of the control plane.

Automated Updates: EKS automatically updates the Kubernetes version, eliminating the need for manual intervention and ensuring that the cluster stays up-to-date with the latest features and security patches.

Scalability: EKS can automatically scale the Kubernetes control plane based on demand, ensuring the cluster remains responsive as the workload increases.

AWS Integration: EKS seamlessly integrates with various AWS services, such as AWS IAM for authentication and authorization, Amazon VPC for networking, and AWS Load Balancers for service exposure.

Security and Compliance: EKS is designed to meet various security standards and compliance requirements, providing a secure and compliant environment for running containerized workloads.

Monitoring and Logging: EKS integrates with AWS CloudWatch for monitoring cluster health and performance metrics, making it easier to track and troubleshoot issues.

Ecosystem and Community: Being a managed service, EKS benefits from continuous improvement, support, and contributions from the broader Kubernetes community.

#### Cons:
Cost: EKS is a managed service, and this convenience comes at a cost. Running an EKS cluster may be more expensive compared to self-managed Kubernetes, especially for large-scale deployments.

Less Control: While EKS provides a great deal of automation, it also means that you have less control over the underlying infrastructure and some Kubernetes configurations.

#### Self-Managed Kubernetes on EC2 Instances Pros:
Cost-Effective: Self-managed Kubernetes allows you to take advantage of EC2 spot instances and reserved instances, potentially reducing the overall cost of running Kubernetes clusters.

Flexibility: With self-managed Kubernetes, you have full control over the cluster's configuration and infrastructure, enabling customization and optimization for specific use cases.

EKS-Compatible: Self-managed Kubernetes on AWS can still leverage various AWS services and features, enabling integration with existing AWS resources.

Experimental Features: Self-managed Kubernetes allows you to experiment with the latest Kubernetes features and versions before they are officially supported by EKS.
#### Cons:

Complexity: Setting up and managing a self-managed Kubernetes cluster can be complex and time-consuming, especially for those new to Kubernetes or AWS.

Maintenance Overhead: Self-managed clusters require manual management of Kubernetes control plane updates, patches, and high availability.

Scaling Challenges: Scaling the control plane of a self-managed cluster can be challenging, and it requires careful planning to ensure high availability during scaling events.

Security and Compliance: Self-managed clusters may require additional effort to implement best practices for security and compliance compared to EKS, which comes with some built-in security features.

Lack of Automation: Self-managed Kubernetes requires more manual intervention and scripting for certain operations, which can increase the risk of human error.

### Setting up your AWS Environment for EKS
### Creating an AWS Account and Setting up IAM Users
Creating an AWS account is the first step to access and utilize AWS services, including Amazon Elastic Kubernetes Service (EKS). Here's a step-by-step guide to creating an AWS account and setting up IAM users:

Create an AWS Account:

Go to the AWS website (https://aws.amazon.com/) and click on the "Create an AWS Account" button.
Follow the on-screen instructions to provide your email address, password, and required account details.
Enter your payment information to verify your identity and set up billing.
Access AWS Management Console:

After creating the account, you will receive a verification email. Follow the link in the email to verify your account.
Log in to the AWS Management Console using your email address and password.
Set up Multi-Factor Authentication (MFA) (Optional but recommended):

Once you are logged in, set up MFA to add an extra layer of security to your AWS account. You can use MFA with a virtual MFA device or a hardware MFA device.
Create IAM Users:

Go to the IAM (Identity and Access Management) service in the AWS Management Console.
Click on "Users" in the left-hand navigation pane and then click on "Add user."
Enter a username for the new IAM user and select the access type (Programmatic access, AWS Management Console access, or both).
Choose the permissions for the IAM user by adding them to one or more IAM groups or attaching policies directly.
Optionally, set permissions boundary, tags, and enable MFA for the IAM user.
Access Keys (for Programmatic Access):

If you selected "Programmatic access" during user creation, you will receive access keys (Access Key ID and Secret Access Key).
Store these access keys securely, as they will be used to authenticate API requests made to AWS services.
