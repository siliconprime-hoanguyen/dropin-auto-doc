# dropin-auto-doc

## DevAPI: https://apiautodev.dropininc.com


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
