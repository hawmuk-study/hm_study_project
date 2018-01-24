# README

*쇼핑몰을 만들어 보는 스터디*



# tree
```
HM_STUDY -- .config_secret -- settings_common.json
                           |- settings_debug.json
                           |- settings_deploy.json
```
 - settings_common.json
 
 ```
 {
 	"django":{
 		"secret_key":"<key>"
 		}
 }
 ```
 - settings_debug.json
 
 ```
 {
 	"django":{
 		"allowed_hosts": "*"
 		}
 }
 ```
 - settings_deploy.json
 
 ```
 {
  "django":{
    "allowed_hosts":[
      "localhost",
      ".compute.amazonaws.com",
      ".elasticbeanstalk.com",
      ""
    ],
  "databases":{
    "default":{
      "ENGINE":"django.db.backends.postgresql",
      "NAME":"",
      "USER":"",
      "PASSWORD":"",
      "HOST":"",
      "PORT":"5432"
      }
    }
  },
  "aws":{
      "access_key_id" :"",
      "secret_access_key":"",
      "s3_bucket_name":"",
      "s3_signature_version":"s3v4",
      "s3_region_name":"ap-northeast-2"
    }
}

 ``` 
 

# Setup
 - django 2.0 , python 3.6

# Config
 - Migrations is not include
 - Please make migrate
 - You must enter ```export DJANGO_SETTINGS_MODULE=config.settings.(debug|deploy)``` to do migrate in terminal
