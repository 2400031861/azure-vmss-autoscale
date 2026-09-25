# Azure VMSS Autoscale

## Project Overview

This project demonstrates how to deploy and configure an Azure Virtual Machine Scale Set (VMSS) with autoscaling based on CPU utilization.

## Azure Services Used

* Azure Virtual Machine Scale Sets
* Azure Virtual Network
* Azure Network Security Group
* Azure Monitor
* Azure Autoscale
* Azure Virtual Machines
* Azure Resource Group

## Autoscaling Configuration

The VM Scale Set is configured with:

* Minimum instances: 2
* Maximum instances: 5
* Default instances: 2
* Scale out when average CPU usage is greater than 70%
* Increase instance count by 1
* Scale in when average CPU usage is less than 30%
* Decrease instance count by 1

## CPU Load Testing

CPU load was generated on the Linux VM using the `stress` utility:

```bash
sudo apt update
sudo apt install -y stress
stress --cpu 2 --timeout 600
```

## Project Screenshots

### 1. Resource Group

![Resource Group](screenshots/01-resource-group.png)

### 2. VMSS Validation

![VMSS Validation](screenshots/02-vmss-validation.png)

### 3. VMSS Deployment

![VMSS Deployment](screenshots/03-vmss-deployment.png)

### 4. Initial VMSS Instances

![Initial Instances](screenshots/04-initial-instances.png)

### 5. Autoscale Limits

![Autoscale Limits](screenshots/05-autoscale-limits.png)

### 6. Autoscale Rules

![Autoscale Rules](screenshots/06-vmss-autoscale-rules.png.png)

### 7. VMSS Metrics

![VMSS Metrics](screenshots/07-vmss-metrics.png.png)

### 8. CPU Metrics

![CPU Metrics](screenshots/08-vmss-cpu-metrics.png.png)

### 9. VMSS Instances

![VMSS Instances](screenshots/09-vmss-instances.png)

### 10. SSH Inbound Rule

![SSH Inbound Rule](screenshots/10-ssh-inbound-rule.png.png)

### 11. CPU Load Test

![CPU Load Test](screenshots/11-cpu-load-test.png.png)

### 12. Final Autoscale Configuration

![Final Autoscale](screenshots/12-autoscale-final.png.png)

## Result

The Azure VM Scale Set was successfully configured with CPU-based autoscaling. The project demonstrates scaling out when CPU utilization increases and scaling in when CPU utilization decreases.
