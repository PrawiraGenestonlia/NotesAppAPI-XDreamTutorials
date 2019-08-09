Service Information
service: notes-app-api
stage: prod
region: us-west-2
stack: notes-app-api-prod
resources: 35
api keys:
  None
endpoints:
  POST - https://wabtm9y7pi.execute-api.us-west-2.amazonaws.com/prod/notes
  GET - https://wabtm9y7pi.execute-api.us-west-2.amazonaws.com/prod/notes/{id}
  GET - https://wabtm9y7pi.execute-api.us-west-2.amazonaws.com/prod/notes
  PUT - https://wabtm9y7pi.execute-api.us-west-2.amazonaws.com/prod/notes/{id}
  DELETE - https://wabtm9y7pi.execute-api.us-west-2.amazonaws.com/prod/notes/{id}
functions:
  create: notes-app-api-prod-create
  get: notes-app-api-prod-get
  list: notes-app-api-prod-list
  update: notes-app-api-prod-update
  delete: notes-app-api-prod-delete
layers:
  None
Serverless: Run the "serverless" command to setup monitoring, troubleshooting and testing.

--- TEST --- (aws-api-gateway-cli-test)
apig-test --username prawira.96@gmail.com --password Prawira96 --user-pool-id us-west-2_zoelIIwPx --app-client-id 1pm7vunr6ifqp0970430jep0h1 --cognito-region us-west-2 --identity-pool-id us-west-2:5859dd7c-2e15-438b-8fb4-fe308575ffc5 --invoke-url https://wabtm9y7pi.execute-api.us-west-2.amazonaws.com/prod --api-gateway-region us-west-2 --path-template /notes --method POST --body "{\"content\":\"hello world\",\"attachment\":\"hello.jpg\"}"
