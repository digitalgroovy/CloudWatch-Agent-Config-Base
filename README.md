# CloudWatch-Agent-Config-Base
Basic configuration file for CloudWatch Agent installation on an EC2 Instance. 

	After cloudwatch agent deb file has been installed, add this repo's json file. cd /opt/aws/amazon-cloudwatch-		agent/etc/amazon-cloudwatch-agent.d   this directory should be empty initally.
	
	Create a new confg file in the aforementioned directory using vim by: vi cloudwatchconfig.cfg
	Switch vim to insert mode and paste in the json file.
	
	



Notes: 1) File path specified needs to be changed per each instance set up.
       2) Log group name and log stream name should be changed from "test" to usage type for prod.
       3) More metrics are available and can be added for measurement. Review aws documentation. 
       4) Intervals should be changed depending on use case.
       
       
       


