# dropin-auto-doc

## DevAPI: https://apiautodev.dropininc.com

## DevWeb: https://autodev.dropininc.com

## ProdAPI: https://apiprodauto.dropininc.com/

## ProdWeb: https://auto.dropininc.com/


### API key is required for every call to server, adding the below key/value pair to header

```javascript
{apikey: xxxxx}
```




## Dashboard


### Getting organizations

```javascript
GET /dashboard/getorganizations?query=xxx
```

#### Query

```javascript
{
  name:'xxx' //organization name
  skip: 10,
  limit: 20
}
```



### Getting call csv file

```javascript
GET /dashboard/exportcsvcalls?query=xxx
```

#### Query

```javascript
{
  name:'xxx' //firstName or lastName
  phone: 'xxx',
  organizationName: 'xxx',
  status: 'missed,completed,expired',
  carType: 'sedan',
  carModel: 'camry'
  carMake: 'toyota',
  from: '2016-06-16',
  to: '2016-06-16',
  vin: '12321',
  skip: 10,
  limit: 20,
  timezoneoffset: -420 //for GMT+7, default:0
}
```


### Getting call

```javascript
GET /dashboard/getcalls?query=xxx
```

#### Query

```javascript
{
  name:'xxx' //firstName or lastName
  phone: 'xxx',
  organizationName: 'xxx',
  status: 'missed,completed,expired',
  carType: 'sedan',
  carModel: 'camry'
  carMake: 'toyota',
  from: '2016-06-16',
  to: '2016-06-16',
  vin: '12321',
  skip: 10,
  limit: 20,
  timezoneoffset: -420 //for GMT+7, default:0
}
```


### Getting dealers for organization

```javascript
GET /organization/getdealers?organizationId=xxxx&query=....
```

#### Query

```javascript
{
  name:'xxx' //firstName or lastName
  phone: 'xxx',
  email: 'xxx',
  organizationName: 'xxx',
  organizationId: 'xxx',
  status: 'active,inactive',
  accountStatus: 'online,offline',
  from: '2016-06-16',
  to: '2016-06-16',
  skip: 10,
  limit: 20,
}
```

### Counting dealers for organization

```javascript
GET /organization/countdealer?organizationId=xxxx&query=....
```

#### Query

```javascript
{
  name:'xxx' //firstName or lastName
  phone: 'xxx',
  email: 'xxx',
  organizationName: 'xxx',
  organizationId: 'xxx',
  status: 'active,inactive',
  accountStatus: 'online,offline',
  from: '2016-06-16',
  to: '2016-06-16'
}
```



### Export lead csv file

```javascript
GET /dashboard/exportcsvleads?query=xxx
```

#### Query

```javascript
{
  name:'xxx' //firstName or lastName
  phone: 'xxx',
  organizationName: 'xxx',
  status: 'missed,completed,expired',
  carType: 'sedan',
  carModel: 'camry'
  carMake: 'toyota',
  from: '2016-06-16',
  to: '2016-06-16',
  vin: '12321',
  skip: 10,
  limit: 20,
  timezoneoffset: -420 //for GMT+7, default:0
}
```


### Getting lead

```javascript
GET /dashboard/getleads?query=xxx
```

#### Query

```javascript
{
  name:'xxx' //firstName or lastName
  phone: 'xxx',
  organizationName: 'xxx',
  status: 'missed,completed,expired',
  carType: 'sedan',
  carModel: 'camry'
  carMake: 'toyota',
  from: '2016-06-16',
  to: '2016-06-16',
  vin: '12321',
  skip: 10,
  limit: 20,
  timezoneoffset: -420 //for GMT+7, default:0
}
```
### Counting lead and call by range

```javascript
GET /dashboard/countcalllead?query=xxx
```

#### Query

```javascript
{
  from: '2016-06-16',
  to: '2016-06-16',
 }
```

### Counting all lead and call

```javascript
GET /dashboard/countallcalllead
```

### Counting lead

```javascript
GET /dashboard/countlead?query=xxx
```

#### Query

```javascript
{
  name:'xxx' //firstName or lastName
  phone: 'xxx',
  organizationName: 'xxx',
  status: 'missed,completed,expired',
  carType: 'sedan',
  carModel: 'camry'
  carMake: 'toyota',
  from: '2016-06-16',
  to: '2016-06-16',
  vin: '12321'
}
```

### Counting call

```javascript
GET /dashboard/countcall?query=xxx
```

#### Query

```javascript
{
  name:'xxx' //firstName or lastName
  phone: 'xxx',
  organizationName: 'xxx',
  status: 'missed,completed,expired',
  carType: 'sedan',
  carModel: 'camry'
  carMake: 'toyota',
  from: '2016-06-16',
  to: '2016-06-16',
  vin: '12321'
}
```


### For requests which need authentication, please add this to the headers of the requests

```javascript
{
  Authorization: 'JWT xxxxxx'
}
```

## Stream


### Log stream for receving web socket messages, push notification messages)

```javascript
POST /streams/log/:streamId
```


#### Body

```javascript
{
"type":"pusher",
"code":3
}
```


### Get vin model

```javascript
GET /vin/:vinId
```



### Get stream list (Authentication required)

```javascript
GET /streams
```



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
GET /streams/:streamId 
```


### Pinging for dealer (Authentication required)
#### Failure on pinging server during 'streaming' session from dealer's behalf will result in the expiration of the session.

```javascript
POST /ping
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

### Sending loan link to customer after stream is finished.

```javascript
POST /streams/sendloanlink/:streamId
```



### Feedback streaming

```javascript
POST /leads
```

#### The caller MUST provide streamId or (organizationToken and vinId), all are provided, streamId will be used.

#### Body

```javascript
{
    "streamId":"dfdsfsdf",
    "organizationToken":"organizationninh0",
    "vinId": "123",
    "email":"hoa@codehub.io",
    "lastName":"hoa",
    "firstName": "hoa",
    "phone":"dfdsfds",
    "comment": "123213"
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

### Logout (Authentication required)

```javascript
POST /auth/logout
```

### Switch online (Authentication required)

```javascript
POST /accounts/status/online
```

### Switch offline (Authentication required)

```javascript
POST /accounts/status/offline 
```



## Chat

### Save chat message

```javascript
POST /chat/:streamId
```

#### Body
```javascript
{
"from":"accountId",
"message":"xxxx"
}
```

### Get chat history

```javascript
GET /chat/:streamId?start=0&limit=10
```



### Login 

#### For this API, mobile caller MUST provide header

```javascript
 Plaform: ['ios', 'android'] //one of the 2 values
```


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
