.PHONY: build 

build: 
	sam build 

deploy-infra: 
	sam build && aws-vault exec oab-crc --no-session --  sam deploy 

deploy-site:
	aws-vault exec oab-crc --no-session --  aws s3 sync ./resume-site s3://oab-crc-website 

invoke get-function: 
	sam build && aws-vault exec oab-crc --no-session --  sam local invoke GetFunction

invoke put-function: 
	sam build && aws-vault exec oab-crc --no-session --  sam local invoke PutFunction 