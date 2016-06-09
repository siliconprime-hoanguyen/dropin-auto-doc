```javascript
{
  "streamMessages": {
    "streamRequested": {
      "code": 0,
      "title": "requested",
      "message": "requested"
    },
    "streamAccepted": {
      "code": 1,
      "title": "accepted",
      "message": "accepted"
    },
    "streamCancelled": {
      "code": 2,
      "title": "cancelled",
      "message": "canclled"
    },
    "streamStopped": {
      "code": 3,
      "title": "stopped",
      "message": "stopped"
    },
    "streaming": {
      "code": 4,
      "title": "streaming",
      "message": "streaming"
    },
    "streamExpired": {
      "code": 5,
      "title": "expired",
      "message": "expired"
    }
  },
  "errorMessages": {
    "organizationNotAvailable": {
      "code": "ERROR_ORGANIZATION_NOT_AVAILABLE",
      "status": 400,
      "message": "This organization is not available"
    },
    "dealerNotFound": {
      "code": "ERROR_DEALER_NOT_FOUND",
      "status": 400,
      "message": "No available dealer found for this organization"
    },
    "invalidActionStream": {
      "code": "ERROR_ACTION_STREAM_INVALID",
      "status": 400,
      "message": "This action cannot be performed on this stream or this stream does not exist"
    },
    "invalidOrganizationToken": {
      "code": "ERROR_TOKEN_INVALID",
      "status": 400,
      "message": "This token does not exist"
    },
    "failureOnOpenTokSession": {
      "code": "ERROR_OPENTOK_SESSION",
      "status": 400,
      "message": "OpentTok failed to create session"
    },
    "alreadyAcceptedStream": {
      "code": "ERROR_STREAM_IS_ON_THE_WAY",
      "status": 400,
      "message": "This stream is not available anymore"
    },
    "busyDealer": {
      "code": "ERROR_BUSY_DEALER",
      "status": 400,
      "message": "This dealer must stop his/her current stream before accepting a new one"
    },
    "loginFailed": {
      "code": "ERROR_INVALID_CREDENTIALS",
      "status": 400,
      "message": "Invalid credentials provided"
    },
    "accountNotExist": {
      "code": "ERROR_INVALID_ACCOUNT",
      "status": 400,
      "message": "This account does not exists"
    },
    "invalidSessionId": {
      "code": "ERROR_INVALID_SESSIONID",
      "status": 400,
      "message": "This sessionId is invalid or being used"
    },
    "invalidStreamId": {
      "code": "ERROR_INVALID_STREAMID",
      "status": 400,
      "message": "This streamId does not exist"
    },
    "createLeadFailed": {
      "code": "ERROR_CANNOT_CREATE_LEAD",
      "status": 400,
      "message": "The information is not enough for creating lead"
    }
  }
}


```
