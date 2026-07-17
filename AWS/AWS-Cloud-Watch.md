# AWS CloudWatch Notes

## What is CloudWatch?

CloudWatch is AWS's monitoring and observability service.

It monitors: - CPU Utilization - Network In / Out - Disk I/O - Status
Checks

> Memory (RAM) monitoring requires the CloudWatch Agent.

## CloudWatch Components

### Metrics

-   Collect numerical performance data.
-   Examples: CPU, Network, Disk.
-   Metrics only collect data.

### Alarms

-   Watch metrics.
-   Trigger actions when thresholds are crossed.
-   Can:
    -   Send SNS notifications
    -   Trigger Auto Scaling
    -   Invoke Lambda

### Logs

-   Store application and system logs.
-   Help determine WHY an application failed.

Examples: - Database connection timeout - Access denied - Application
exception

### CloudWatch Agent

Required for: - RAM metrics - Disk usage - Application logs - System
logs

## Metrics vs Logs

  Metrics               Logs
  --------------------- -------------------------
  Performance numbers   Error/details
  CPU, Network, Disk    Application/System logs
  Monitoring            Troubleshooting

## CloudWatch + ASG Flow

EC2 ↓ CloudWatch Metrics ↓ CloudWatch Alarm ↓ Auto Scaling Group ↓
Launch EC2 (from AMI) ↓ Load Balancer Health Check ↓ Traffic routed to
new EC2

## Production Troubleshooting

1.  Check CloudWatch Metrics.
2.  If infrastructure is healthy:
    -   Check CloudWatch Logs.
3.  Find root cause.
4.  Fix issue.

## Common Interview Points

-   Metrics collect data.
-   Alarms evaluate metrics and trigger actions.
-   CloudWatch does not create EC2.
-   Auto Scaling creates/terminates EC2.
-   Load Balancer sends traffic only to healthy instances.
-   CloudWatch Agent is required for RAM metrics and application logs.

## Key Revision

-   CloudWatch Metrics
-   CloudWatch Alarms
-   CloudWatch Logs
-   CloudWatch Agent
-   Metrics vs Logs
-   CloudWatch + ASG Integration
-   Production troubleshooting workflow
