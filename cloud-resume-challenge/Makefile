.PHONY: build 

build: 
	sam build 

deploy-infra: 
	sam build && aws-vault exec oab-crc --no-session --  sam deploy 

deploy-site:
	aws-vault exec oab-crc --no-session --  aws s3 sync ./resume-site s3://oab-crc-website 