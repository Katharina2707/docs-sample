# Custom Alerts User Guide

Welcome to the **Custom Alerts** feature in the cloud dashboard! This guide will help you set up your first alert and explore advanced configuration options.

You can set up alerts for CPU usage, memory, and network thresholds. The feature is designed to be intuitive for beginners and powerful for advanced users. 

## Getting started: Set up your first alert

1. **Log in to the cloud dashboard**  
   Navigate to your cloud dashboard and log in with your credentials.

2. **Access the Alerts section**  
   From the main menu, go to **Monitoring > Alerts**.

3. **Create a new alert**  
   Click the **Create Alert** button.

4. **Choose a metric**  
   Select one of the available metrics:
   - CPU Usage
   - Memory Usage
   - Network Throughput

5. **Set thresholds**  
   Define the threshold value that will trigger the alert. For example:
   - CPU Usage > 80%
   - Memory Usage > 75%
   - Network Throughput > 100 Mbps

6. **Configure notification settings**  
   Choose how you want to be notified:
   - Email
   - SMS
   - Webhook

7. **Save the alert**  
   Click **Save** to activate your alert.


## Advanced configuration: Compound Conditions

Experienced users can create alerts based on **Compound Conditions**, combining multiple metrics using logical operators. For example:  

`Trigger alert if CPU Usage > 80% AND Memory Usage > 70%`

This allows for more precise monitoring and reduces false positives.







