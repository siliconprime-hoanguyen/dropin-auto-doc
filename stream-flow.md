# Streaming flow from end user perspective

## Customer View:

### 1. Customer starts a streaming request R to an organization.

#### 1.1 If no dealer ~~has logged in,~~ OR all dealers are IN THE MIDDLE OF THEIR REQUESTS, ACTIVE STREAMING SESSION, OR all dealers are OFFLINE, server informs web, and web informs customer.

#### 1.2 If at least 1 dealer, given B, ~~has logged in, and~~ is ONLINE, and is NOT IN THE MIDDLE OF ANY REQUEST, ACTIVE STREAMING SESSION, server sends the request to B.

- If web does not receive the response within 0 - 30 seconds, web go to step 1.

- If web receives the response within 0 - 30 seconds, web go to step 2.


### 2. Streaming, after done, go to step 3.

### 3. END

## Dealer View

### 1. Dealer receives the request.

### 2. Dealer processes the request

- 2.1 If dealer accepts the request within 0 - 30 seconds, app informs dealer and dealer goes to step 3.

- 2.2 If dealer accepts the request after 30 seconds, server returns error to app, app informs dealer and dealer goes to step 4.

- 2.3 Dealer leaves the request as is, go to step 4

### 3. Streaming, after done, go to step 4.

### 4. END

## Some cases might prevent dealers from receiving request
- Dealer is NOT active (set by admin in dashboard)
- Dealer is NOT online (set by dealer himself in the app)
- Dealer is in middle of a request of an active streaming.
- Given both dealer A and dealer B are online in the same organization C and free, the last ping of dealer A to server is at 10PM, the last ping of dealer B to server is at 11PM, any request to organization C will come to dealer B first.
Now, dealer B logouts, the request still comes to dealer B FIRST, UNTIL the next ping of user A.
