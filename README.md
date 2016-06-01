# dropin-auto-doc

# DevAPI: http://dropin-dev-auto-api.us-west-2.elasticbeanstalk.com


## Stream

### Request stream

```javascript
POST /streams/request/:organizationCode
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
