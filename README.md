# dropin-auto-doc

## DevAPI: https://apiautodev.dropininc.com

### For requests which need authentication, please add this to the headers of the requests

```javascript
{
  Authorization: 'JWT xxxxxx'
}
```

## Stream

### Request stream

```javascript
POST /streams/request/:organizationCode
```


#### Body

```javascript
{
"vin":"xxx",
}
```

### Accept stream (Authentication required)

```javascript
POST /streams/accept/:streamId 
```


### Stop stream

```javascript
POST /streams/stop/:streamId 
```


### Get stream

```javascript
POST /streams/:streamId 
```


### Ping stream (Authentication required)
#### Failure on pinging server during 'streaming' session from dealer's behalf will result in the expiration of the session.

```javascript
POST /streams/ping/:streamId 
```

### Add/edit note for the stream (stream MUST be stopped or completed)

```javascript
POST /streams/note/:streamId 
```

#### Body

```javascript
{
"note":"xxx",
}
```


## Socket

### Authentication for Pusher service URL (called by Pusher SDK)

```javascript
POST /socket/auth
```

#### Body

```javascript
{
"socket_id":"xxx",
"channel_name":"xxxx"
}
```


## Account

### Register 

```javascript
POST /auth/register
```

#### Body
```javascript
{
"email":"xxx@xxx.com",
"password":"xxxxxx",
"firstName":"xxxx",
"lastName":"xxx",
"username":"xxxxx"
}
```
### Register 

```javascript
POST /auth/changepassword
```

#### Body
```javascript
{
"username":"xxxxx",
"password":"xxxx",
"newpassword":"xxxxxx"
}
```


### Login 

```javascript
POST /auth
```


#### Body

#### Only email OR username is used.
```javascript
{
"email":"xxx@xxx.com",
"username":"xxxxx"
"password":"xxxxxx",
}
```
