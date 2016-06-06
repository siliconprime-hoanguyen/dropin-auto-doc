```javascript
['requested', // the initial status of the streaming, right after viewer requests a new stream.
 'missed', // no dealer responses the request
 'expired', // dealer does not ping when streaming for more than 10 minutes
 'streaming', // the streaming is on going.
 'stopped', // the streaming has just been stopped
 'completed', //the streaming stopped and given note/feedback by viewer/dealer
 ]
```
