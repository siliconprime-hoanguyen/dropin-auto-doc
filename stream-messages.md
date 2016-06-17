{
  "streamMessages": {
    "streamRequested": {
      "code": 0,
      "title": "You have a new video tour request",
      "message": "You have a new video tour request"
    },
    "streamAccepted": {
      "code": 1,
      "title": "accepted",
      "message": "accepted"
    },
    "streamCancelled": {
      "code": 2,
      "title": "Video tour request cancelled",
      "message": "Video tour request cancelled"
    },
    "streamStopped": {
      "code": 3,
      "title": "Video tour completed",
      "message": "Video tour completed"
    },
    "streaming": {
      "code": 4,
      "title": "streaming",
      "message": "streaming"
    },
    "streamExpired": {
      "code": 5,
      "title": "Dealer is offline while streaming",
      "message": "This dealer has been offline for more than 10 minutes while in streaming"
    },
    "streamOccupied": {
      "code": 6,
      "title": "The request was occupied by ",
      "message": "The request was occupied by "
    },
    "streamMissed": {
      "code": 7,
      "title": "You have missed a request ",
      "message": "You have missed a request, please go to your call list to review"
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
      "message": "This stream was occupied by "
    },
    "busyDealer": {
      "code": "ERROR_BUSY_DEALER",
      "status": 400,
      "message": "This dealer must stop his/her current stream before accepting a new one"
    },
    "offlineDealer": {
      "code": "ERROR_OFFLINE_DEALER",
      "status": 400,
      "message": "This dealer failed to go online for a long time, therefore cannot accept this tream"
    },
    "noOnlineDealer": {
      "code": "ERROR_NO_ONLINE_DEALER",
      "status": 400,
      "message": "At least a dealer detected but he/she is not available for streaming"
    },
    "loginFailed": {
      "code": "ERROR_INVALID_CREDENTIALS",
      "status": 403,
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
    "criticalStreamingFlowError": {
      "code": "ERROR_CRITICAL_FLOW_ERROR",
      "status": 400,
      "message": "This error is critical"
    },
    "createLeadFailed": {
      "code": "ERROR_CANNOT_CREATE_LEAD",
      "status": 400,
      "message": "The information is not enough for creating lead"
    },
    "invalidPlatform": {
      "code": "ERROR_INVALID_PLATFORM",
      "status": 403,
      "message": "The user is not allowed to login on this platform"
    },
    "emailUserNameDuplicated": {
      "code": "ERROR_DUPLICATION",
      "status": 400,
      "message": "This email or username is/are already in use"
    },
    "invalidPasswordLength": {
      "code": "ERROR_PASSWORD_LENGTH",
      "status": 400,
      "message": "Password length must be more than 5"
    },
    "invalidInfoType": {
      "code": "ERROR_INFO_TYPE",
      "status": 400,
      "message": "The requested type is invalid"
    },
    "noEmailAndPhone": {
      "code": "ERROR_NO_EMAIL_PHONE",
      "status": 400,
      "message": "The lead did not provide phone and email"
    },
    "noCreditApplicationUrl": {
      "code": "ERROR_NO_CREDIT_APP_URL",
      "status": 400,
      "message": "The organization does not have credit application url, please login as admin end provide the credit application url for it"
    }
  },
  "smsMessages": {
    "loanLink": "Hi %name%! We appreciate your interest in our vehicle! Here’s the link to our loan approval/pre-approval you have requested, I look forward to your visit! %link%"
  }
}
