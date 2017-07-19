# nationalparks-conversation
 
The repo contains code demonstrating the Watson Conversation service


![](https://github.com/cdimascio/nationalparks_conversation/raw/master/.assets/sshot.png)

## Prequisities

1. Clone this repo
2. Create a Bluemix account

## Setup

### Conversation

- Provision an instance of [Watson Conversation](https://console.bluemix.net/catalog/services/conversation?env_id=ibm:yp:us-south&taxonomyNavigation=services) on Bluemix
- Create a new conversation workspace by importing `./resources/conversation_workspace.json` into your Watson Conversation workspaces,
- Install client and server dependencies
- Create `.env` files in the project root with the following contents

```
APP_ID=parks-conversation
PORT=3004
LOG_LEVEL=debug
SESSION_SECRET=test

WATSON_CONVERSATION_API_ROOT=https://gateway.watsonplatform.net/conversation/api
WATSON_CONVERSATION_VERSION=v1
WATSON_CONVERSATION_VERSION_DATE=2016-07-11
WATSON_CONVERSATION_USERNAME=<USERNAME>
WATSON_CONVERSATION_PASSWORD=<PASSWORD>
WATSON_CONVERSATION_WORKSPACE_ID=<WORKSPACE>
```

### Server
- `npm install`

### Client
- `cd client`
- `npm install`

## Build / Run (Development)
- Start the server `npm start`
- Start the client `cd client && npm start`
- Navigate to http://localhost:3000

## Build / Run (Production)
- `cd client`
- `npm run build`
- `cd ..`
- `npm start`
- Navigate to http://localhost:3000

## Deploy to Bluemix
Follow the first 3 steps in the "Build / Run (Production)" section above, then run:

- `cf push nationalparks`

