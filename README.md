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
