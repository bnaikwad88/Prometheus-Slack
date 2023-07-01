# Prometheus Monitoring and Alerting for Multiple EC2 Instances in Multiple Accounts with Slack Integration

## Objective :
To create a Prometheus monitoring system for multiple Amazon Elastic Compute Cloud (EC2) instances in multiple accounts and send alerts to a Slack community when any of the servers are down

## Expected Results : 
The result of setting up a Prometheus monitoring system for multiple EC2 instances in multiple accounts and sending alerts to a Slack community when any of the servers are down should be a system that can monitor the status of the EC2 instances and send notifications to the Slack channel if any of the servers are down.

## Some potential benefits of this system may include: 
### Improved uptime :
By monitoring the status of the EC2 instances and being alerted when any of them go down, you can take action to restore service as quickly as possible. 
### Increased visibility:
The Prometheus server and exporters will collect a wide range of metrics about the performance and health of the EC2 instances, which can help you identify trends and issues that may not be immediately apparent. 
### Enhanced collaboration:
By sending alerts to a Slack channel, you can make it easier for team members to stay informed about the status of the EC2 instances and collaborate on resolving any issues that arise. 
<br>**Overall, the result of this system should be a more reliable, transparent, and collaborative way to manage the EC2 instances in your environment.**<br/>
# Approach
## To create a Prometheus monitoring system for multiple Amazon Elastic Compute Cloud (EC2) instances in multiple accounts and send alerts to a Slack community when any of the servers are down, you will need to perform the following steps:
1. Set up a Prometheus server on one of the EC2 instances. This can be done by following the instructions in the Prometheus documentation.
2. Set up one or more Prometheus exporters on each of the other EC2 instances that you want to monitor. An exporter is a piece of software that runs on a host and exposes metrics in a format that Prometheus can scrape. There are many exporters available for different types of systems, such as the Node Exporter for Linux servers and the MySQL Exporter for databases.
3. Configure the Prometheus server to scrape metrics from the exporters. This can be done by modifying the configuration file for the server and adding a job configuration for each exporter.
4. Set up an alerting rule in Prometheus to send a notification to a Slack channel when a server goes down. This can be done by modifying the configuration file for the server and adding an alerting rule that specifies the condition under which the alert should be triggered and the Slack webhook to which the alert should be sent.
5. Test the system to ensure that it is working as expected. This can be done by simulating a server failure and verifying that the alert is sent to the Slack channel.
## Results:
+ Prometheus UP and RUNNING
 ![prometheus_status](https://github.com/bnaikwad88/Prometheus-Slack/assets/116859424/6df3e868-586b-4f60-9343-aa79a96d2b41)
+ Alertmanager UP and RUNNING
 ![alertmanager_status](https://github.com/bnaikwad88/Prometheus-Slack/assets/116859424/69ef6453-ff05-44be-99c8-38a1af41a622)
+ Node_Exporter 1 Active
 ![node1_status-active](https://github.com/bnaikwad88/Prometheus-Slack/assets/116859424/0d32f992-bf9e-4c61-be0d-9b00bcbb6db6)
+ Node_Exporter 2 Active
 ![node2_status-active](https://github.com/bnaikwad88/Prometheus-Slack/assets/116859424/95dc6704-6a63-4f85-8e7c-ba7763ed201f)
+ Prometheus(Both Nodes Active)
 ![prometheus_n1n2-up](https://github.com/bnaikwad88/Prometheus-Slack/assets/116859424/b35e92c1-55cc-40d5-99b4-7e1a205bbc30)
+ Prometheus(Both Nodes1 Active Node2 Inactive)
 ![prometheus_n1up-n2down](https://github.com/bnaikwad88/Prometheus-Slack/assets/116859424/9f9d0bae-dda6-490e-853f-6b5012caf429)
+ Alertmanager(Node1 Inactive)
 ![alertmanager_node2-down](https://github.com/bnaikwad88/Prometheus-Slack/assets/116859424/f83c6aa6-58c6-4143-8ad8-28ac0f4dac7f)
+ Slack(Node 1 Inactive)
 ![slack_node1-down](https://github.com/bnaikwad88/Prometheus-Slack/assets/116859424/c0a65437-4c07-46d7-8e4c-e9d0955ffe48)
+ Prometheus(Both Nodes Inactive)
 ![prometheus_n1up-n2down](https://github.com/bnaikwad88/Prometheus-Slack/assets/116859424/6b7f7f7f-6d12-45ea-9563-4cba7bb1dc9b)
+ Alertmanager(Both Nodes Inactive)
 ![alertmanager_n1n2-down](https://github.com/bnaikwad88/Prometheus-Slack/assets/116859424/c6b3259e-353e-4f9d-87e5-f573f3cfcf18)
+ Slack(Both Nodes Inactive)
 ![slack_n1n2-down](https://github.com/bnaikwad88/Prometheus-Slack/assets/116859424/77064650-3ee0-45a4-9feb-4a3d505cae45)
+ Slack(Resolved Issue)
 ![slack_allnode-up](https://github.com/bnaikwad88/Prometheus-Slack/assets/116859424/805e078f-74b9-46d4-a22f-8ffd57680edf)



