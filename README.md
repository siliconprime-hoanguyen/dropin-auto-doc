# dropin-auto-doc

## DevAPI-old: https://apiautodev.dropininc.com
## DevAPI-new: https://apiautodev.dropinauto.com

## DevWeb-old: https://autodev.dropininc.com
## DevWeb-new: https://autodev.dropinauto.com


## QaAPI: http://apiautoqa.dropinauto.com/
## QaWeb: http://autoqa.dropinauto.com/t



## StagingAPI-old: https://apiautostaging.dropininc.com/
## StagingAPI-new: http://salesdemo-api.dropinauto.com/

## StagingWeb-old: https://autostaging.dropininc.com/
## StagingWeb-new: http://salesdemo.dropinauto.com/

## ProdAPI: https://api.dropinauto.com/

## ProdWeb: https://app.dropinauto.com/


### API key is required for every call to server, adding the below key/value pair to header


```javascript
{apikey: xxxxx}
```

### App version is required for every call to server, adding the below key/value pair to header

```javascript
{appversion: value}
```

Value may be 'android_viewer-1.2.0', 'android_dealer-1.2.0', 'ios_dealer-1.2.0', 'ios_viewer-1.2.0', 'web-1.2.0'

#### Note: The version might change and needs to be updated accordingly, but the prefixes are fixed.




## Dashboard


### Getting organizations

```javascript
GET /dashboard/getorganizations?query=xxx (DEPRECATED), please use the below instead
GET /organizations?query=xxx
```


### Editting organizations

```javascript
PUT /organizations/:organizationId
```

#### Body

```javascript
{
  "_id": "57b16c3a81553a9d725d97e5",
  "updatedAt": "2016-08-15T07:16:10.068Z",
  "createdAt": "2016-08-15T07:16:10.068Z",
  "companyType": "viewer",
  "state": "CA",
  "name": "empty org",
  "address": "84 Bach Dang, Phuong 2, Quan Tan Binh",
  "companyPhone": "1647689760",
  "city": "Ho Chi Minh",
  "zipcode": "70000",
  "email": "emptyorg@gmail.com",
  "phone": 1647689760,
  "__v": 0,
  "resources": {
    "creditApplicationUrl": "https://www.dropininc.com/creditapplication.html"
  },
  "longitude": "123.123",
  "latitude": "123.2323",
  "siteToken": "123",
  "isFeatured": false,
  "status": "active"
}
```




### Getting call csv file

```javascript
GET /dashboard/exportcsvcalls?query=xxx
```

#### Query

```javascript
{
  name:'xxx', //firstName or lastName
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
  timezoneoffset: -420, //for GMT+7, default:0
  guestId: 'baxxxx', //optional, for history retrieval
  sortBy: 'fieldName',
  sortOrder: 1 //1: ascending, -1: descending
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
  timezoneoffset: -420, //for GMT+7, default:0
  guestId: 'baxxxx', //optional, for history retrieval
 sortBy: 'fieldName',
  sortOrder: 1 //1: ascending, -1: descending
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
  sortBy: 'fieldName',
  sortOrder: 1 //1: ascending, -1: descending
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
  timezoneoffset: -420, //for GMT+7, default:0
  sortBy: 'fieldName',
  sortOrder: 1 //1: ascending, -1: descending
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
  timezoneoffset: -420, //for GMT+7, default:0
 sortBy: 'fieldName',
  sortOrder: 1 //1: ascending, -1: descending
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
  vin: '12321',
  guestId: "baxxxx" //optional, for history retrieval
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
GET /streams?query=xxxx
```


#### Query

```javascript
{
  status:'missed,completed'
}
```


### view car

```javascript
POST /streams/cars/viewcar
```


#### Body

```javascript
{
"vin": "xxx",
"model": "camry", 
"make": "toyota", 
"color": "xxxx", 
"year": 2012
}
```



### Request stream

```javascript
POST /streams/request/:organizationCode
```


#### Body

```javascript
{
"vin": "xxx",
"sessionId": "xxxx", // a unique string provided by app.
"guestId": "baxxxx", //optional, for history retrieval
"deviceAddress": "xxxx", // optional
"deviceType": "xxx" // "ios" or "android"
}
```

### Pickup stream (Authentication required)

```javascript
POST /streams/pickup/:streamId 
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
    "sessionId":"dfdsfsdf",
    "organizationToken":"organizationninh0",
    "vinId": "123",
    "email":"hoa@codehub.io",
    "lastName":"hoa",
    "firstName": "hoa",
    "phone":"dfdsfds",
    "comment": "123213"
}
```


### Follow the stream (stream MUST be stopped or completed or expired)

```javascript
POST /streams/follow/:streamId 
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

### Change password 

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

### Add device

```javascript
POST /devices
```

#### Body
```javascript
{
deviceType:'ios' //or android
deviceAddress:"xxxxxx"
}
```

### Send forgot password link to email

```javascript
POST /auth/forgotpassword
```

#### Body
```javascript
{
"email":"abc@def.com"
}
```


### Get token for requesting password

```javascript
GET /auth/forgotpassword/token=12312
```

### Reset password

```javascript
POST /auth/resetpassword/:token
```
#### Body
```javascript
{
"password":"123456"
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
"from":"572ac19cb4a3f37c5b51081e", //MUST BE 24-CHARACTER LENGHT.
"message":"xxxx"
}
```

### Get chat history

```javascript
GET /chat/:streamId?start=0&limit=10
```



### Get video history

```javascript
GET /organizations/getvideos?organizationId=1111&skip=0&limit=10&name=abc&sortBy=createdAt&sortOrder=-1
```
#### Query

```javascript
{
  organizationId: 'fdsfdsfds', ///organizationid
  skip: 0, //skip how many records
  limit: 10, //get how many records
  name: 'dsfds', //name is for searching by organization name, dealer fullname, dealer username, car model
  sortBy: 'createdAt', //sort by which field?
  sortOrder: -1 //-1: desc, 1: asc
}
```

### Get s3 link for upload (thumbnail, etc)

```javascript
GET /s3/getlink
```


### Update thumbnail for stream

```javascript
POST streams/createthumbnail/:streamId
```

#### Body

```javascript
{
  thumbnailUrl: 'abc'
}
```

### Login 

#### For this API, mobile caller MUST provide header

```javascript
 Platform: ['ios', 'android'] //one of the 2 values
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

## View

### acknowledge/create a view

```javascript
POST /views/
```

### Body
```javascript
{
  "guestId": "test Guest ID", //required
  "organizationId": "57f233e7f51c7a65282914f9", //required
  "vehicleInfo": {
    "model": "Camry", //required       
    "make": "Toyota2", //required  
    "link": "http://toyota.com/new-cars/2016-camry2", //required
    "year": 2016,
    "imageUrl": "https://s3-us-west-1.amazonaws.com/dropin-prod-public-assets-v2/dropin-auto-images/toyota.jpg",
    "type": "sedan"
  }      
}

```

### Get view history

```javascript
GET /views/?guestId=my guest 2&start=0&limit=10
```


