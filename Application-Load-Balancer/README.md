# Application Load Balancer (ALB)

## Objective
To configure an Application Load Balancer to distribute HTTP traffic across multiple EC2 instances and improve availability.

---

## AWS Services Used
- Application Load Balancer
- Amazon EC2
- Target Groups
- Security Groups

---

## Tasks Performed
- Created a target group for EC2 instances
- Registered multiple EC2 instances as targets
- Configured health checks
- Created an internet-facing Application Load Balancer
- Configured HTTP listener to forward traffic to target group
- Verified load balancing using ALB DNS name

---

## Why ALB is Important
Application Load Balancers enable scalable, highly available web applications by distributing traffic and monitoring instance health.

---

## Outcome
- Successfully routed traffic through ALB
- Confirmed healthy targets and traffic distribution

---

## Notes
- Load balancer configured using AWS Free Tier resources
- HTTP used for demonstration purposes
