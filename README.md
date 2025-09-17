# AWS-EC2-PROJECT
## Shared Responsibility Model for EC2

When using Amazon EC2, AWS is responsible for the **security of the cloud**. 
This includes securing the physical infrastructure such as data centers, networking, storage devices, 
and the virtualization layer (the hypervisor) that runs EC2 instances. AWS ensures high availability, 
redundancy, and protection against hardware failures, as well as compliance with global security standards.

As the customer, you are responsible for **security in the cloud**. For EC2, this means managing and patching 
the operating system, securing applications, configuring firewalls through security groups and NACLs, 
controlling access with IAM, encrypting sensitive data, and monitoring logs. Essentially, AWS provides the 
secure foundation, while you must secure everything you build and run on top of EC2.




intsances types and challenges i face
# AWS EC2 Assignment

## Instance Type Comparison
When exploring instance types, I compared **Memory Optimized (r5 family)** and **GPU Optimized (p3 family)**:

- **Memory Optimized (r5)**: Best for workloads that require large amounts of RAM, such as in-memory databases (Redis, SAP HANA) or real-time analytics. They are not designed for heavy CPU or GPU tasks but excel in scenarios where storing and quickly accessing large datasets is critical.
- **GPU Optimized (p3)**: Built for machine learning, artificial intelligence, and high-performance computing (HPC). These instances come with powerful NVIDIA GPUs that accelerate deep learning model training, video rendering, and scientific simulations.

The main takeaway is that **choosing the right instance depends on the workload** — memory-focused vs. compute/GPU-intensive.

---

## Shared Responsibility Model for EC2
AWS and customers share security responsibilities for EC2 instances:

- **What AWS Secures**: AWS manages the underlying infrastructure, including physical hardware, networking, storage, and the hypervisor layer. They ensure data centers are secure, resilient, and compliant with global standards.
- **What Customers Secure**: As a customer, you are responsible for the software running on the instance. This includes updating and patching the operating system, configuring firewalls and security groups, managing IAM access, and securing applications and data.

In short, AWS handles the **security of the cloud**, while customers handle **security in the cloud**.

---

## Challenges and Solutions
1. **Configuring Security Groups**  
   - *Challenge*: I initially set overly open rules, which could allow unnecessary access.  
   - *Solution*: I restricted SSH (port 22) access to my IP only, while allowing HTTP (port 80) for everyone.

2. **Connecting via SSH**  
   - *Challenge*: I got a "Permissions too open" error with my `.pem` key.  
   - *Solution*: I fixed it by running `chmod 400 MyKey.pem` before retrying the SSH command.

3. **Budget Alerts**  
   - *Challenge*: I was worried about overspending on AWS resources.  
   - *Solution*: I set a budget of $5 with alerts at 80%, which helps me monitor costs and stay within safe limits.

---

## Conclusion
This assignment helped me understand the importance of **choosing the right EC2 instance type**, configuring secure access, and applying the shared responsibility model. I also learned practical troubleshooting skills for SSH and budget setup, which are critical for real-world cloud engineering.
