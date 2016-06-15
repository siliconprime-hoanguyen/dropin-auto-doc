```javascript
['requested', // the initial status of the streaming, right after viewer requests a new stream.
 'missed', // at least 1 dealer got the request but none responses
 'expired', // dealer does not ping when streaming for more than 10 minutes
 'streaming', // the streaming is on going.
 'completed', //the streaming stopped.
 'all-offline' // at least 1 dealer logs in but none is active at the moment request comes. 
 ]
```
