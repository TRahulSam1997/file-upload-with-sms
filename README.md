# Twillio sends SMS whenever a new log file is successfully uploaded into a public AWS S3 bucket
I had not worked with AWS S3 bucket before, so I used these 2 projects as a guide:
* https://github.com/khelif96/React-S3-fileuploads
* https://github.com/mimurawil/aws-s3-twilio-notification

Unfortunately, I have come across this error on uploading a file, and I'm still debugging it.
![alt text](https://i.imgur.com/2Go0Au5.png)

## Design decisions / Assumptions
I used the following docs https://www.twilio.com/docs/sms/quickstart/node to connect with Twillio.
At the moment, the following values have to be set in a **.env** file at the root of the project:

* AWSAccessKeyId={}
* AWSSecretKey={}
* Bucket={}
* ACCOUNT_SID={};
* AUTH_TOKEN={};
* TWILIO_PHONE_NO={};
* PHONE_NO_TO_RECEIVE_SMS={};

I have not built a proper user interface for this, yet that will allow the user to add the phone number before uploading the file. Once I do this, I can remove the env variable.

Once the file is uploaded properly, and the response from the bucket is successful, the `handler.js` class will be called, which will send the SMS notification to the user.

## Testing strategies
I would do unit testing with Mocha on the Twilio API and the upload part on the frontend.

## Deployment
Once the upload part works, I will deploy this application on a digital ocean droplet. I will dockerize the application as I can configure the droplet to have docker installed and the deployment will be much easier.

## Issues encountered
There is an issue with the parameters (screenshot attached) I am passing to talk to the S3 bucket, which gives a status code 404.

## Running Project
```
cd twillio
npm install
cd ..
cd backend
npm install
cd ..
npm install
npm start
```