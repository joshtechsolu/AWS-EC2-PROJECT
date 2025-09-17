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

