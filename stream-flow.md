# Streaming flow from end user perspective

## Customer View:

### 1. Customer starts a streaming request R to an organization.

#### 1.1 If no dealer has logged in, OR all dealers are busy, OR all dealers are OFFLINE, server informs web, and web informs customer. Web waits for predecessor requests to be responded (if any)
-  If no response from predecessor requests within 120 seconds from the last request OR this is the 1st request, web goes to step 3.
-  If there is response from predecessor requests, web goes to step 2.

#### 1.2 If at least 1 dealer, given B, has logged in, and is ONLINE, and is NOT BUSY, server sends the request to B.

- If web does not receive the response within 0 - 30 seconds, web go to step 1.

- If web receives the response within 0 - 30 seconds, web go to step 2.


### 2. Streaming, after done, go to step 3.

### 3. END

## Dealer View

### 1. Dealer receives the request.

### 2. Dealer processes the request

- 2.1 If dealer accepts the request within 0 - 120 seconds, app informs dealer and dealer goes to step 3.

- 2.2 If dealer accepts the request after 120 seconds, server returns error to app, app informs dealer and dealer goes to step 4.

- 2.3 Dealer leaves the request as is, go to step 4

### 3. Streaming, after done, go to step 4.

### 4. END
