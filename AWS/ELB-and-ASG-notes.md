# AWS Day 3 Notes -- Elastic Load Balancer (ELB) & Auto Scaling Group (ASG)

## ELB

-   Distributes incoming traffic across healthy EC2 instances.
-   Performs health checks.
-   Stops routing traffic to unhealthy instances.
-   Does not create EC2 instances.

## ASG

-   Automatically launches/terminates EC2 instances.
-   Uses CloudWatch metrics.
-   Launches new EC2 from an AMI.

### Capacity

-   Minimum: Never go below this number.
-   Desired: Number of instances ASG maintains.
-   Maximum: Highest number ASG can launch.

### Scale Out

-   CPU \> 70% → Add EC2.

### Scale In

-   CPU \< 20% → Remove EC2 (never below Minimum).

### Self-Healing

-   If an EC2 crashes, ASG launches a replacement to maintain Desired
    Capacity.

## ELB vs ASG

-   ELB = Traffic Distribution
-   ASG = Instance Management

## Key Takeaways

-   ELB distributes traffic.
-   ELB performs Health Checks.
-   ASG scales out and scales in.
-   ELB + ASG provide scalability and high availability.
