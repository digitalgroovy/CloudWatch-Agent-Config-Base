# CloudWatch-Agent-Config-Base
Basic configuration file for CloudWatch Agent installation on an EC2 Instance. 

Ensure that you have attached CloudWatchAgentServerPolicy and CloudWatchFullAccess to your IAM role being assumed by the EC2 instance. 

After cloudwatch agent deb file has been installed, you will find a directory created at /opt/aws/amazon-cloudwatch-agent/etc/common-config.toml If you have to change or add IAM permissions, you can edit this file with vim or nano.

	
To create a monitoring confg file in the ec2 root directory with vim, copy the json file in this repo and then at prompt: vim agentconfig.cfg (or name it whatever your naming convention requires)
	
Switch vim to insert mode and paste in the json file.

To start it: sudo /opt/aws/amazon-cloudwatch-agent/bin/amazon-cloudwatch-agent-ctl -a fetch-config -m ec2 -c file:agentconfig.cfg -s

To verify the agent started run: sudo service amazon-cloudwatch-agent status	
	
	
	
	Notes: 1) File path specified needs to be changed per each instance set up.
      	 	2) Log group name and log stream name should be changed from "test" to usage type for prod.
       		3) More metrics are available and can be added for measurement. Review aws documentation. 
       		4) Intervals should be changed depending on use case.
       
       
       


