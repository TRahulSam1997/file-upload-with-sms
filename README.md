# Twillio sends SMS whenever a new log file is successfully uploaded into a public AWS S3 bucket
I have not worked with AWS S3 bucket before so I used these 2 projects as a guide:
* https://github.com/khelif96/React-S3-fileuploads
* https://github.com/mimurawil/aws-s3-twilio-notification

Unfortunately, I have come across this error on uploading a file, and I'm still debugging it.
![alt text](https://i.imgur.com/2Go0Au5.png)

## Design decisions / Assumptions
I used the following docs https://www.twilio.com/docs/sms/quickstart/node to connect with Twillio.

## Testing strategies
I would do unit testing with Mocha on the twillio api and the upload part on the frontend.

## Deployment
If the upload app worked

## Issues encountered

## Running Project

`cd twillio`
`npm install`
`cd ..`
`cd backend`
`npm install`
`cd ..`
`npm install`
`npm start`