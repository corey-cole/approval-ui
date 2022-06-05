# AWS Step Functions Approval UI

This project provides a simple UI that can be used to manage approvals across a
collection of state machines that include human approval.

The [canonical example from AWS](https://docs.aws.amazon.com/step-functions/latest/dg/tutorial-human-approval.html) deploys an API gateway and the UI is provided by an email client.

While not yet complete, the intention is to record approval requests in DynamoDB, send a
notification of a pending human interaction, and then allow the application to continue the
workflow using the appropriate task token.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
