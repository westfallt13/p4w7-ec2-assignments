# Amazon EC2 Notes

## Explain why Amazon EC2 stands for "Elastic Compute Cloud." What does the word elastic specifically refer to in cloud architecture?

You can quickly add or remove computing power automatically or on demand, like stretching and relaxing a rubber band.

---

## Name and describe the four essential infrastructure features provided by EC2 that classify it as Infrastructure as a Service (IaaS).

- It provides virtual machines
- It stores data on virtual storage units (EBS - Elastic Block Store)
- It distributes the load across machines (using ELB - Elastic Load Balancer)
- It enables service scaling

---

## Detail the billing model used by EC2. What happens to your costs when you scale down or shut down instances when demand decreases?

They offer a pay-as-you-go model, so you only get billed when instances are running. When you scale down, the billed total goes down with it.

---

## What is the process of bundling configuration commands into a script called?

Bootstrapping

---

## Under which specific user profile are User Data scripts executed?

The root user

---

## How many times does a User Data script run during the lifecycle of an EC2 instance?

They can only run once, during the first boot of the VM, and are not executed again afterwards.