# Node-RED-Dashboard : Log-In, Session

Node-RED Dashboard Example with Sign In (Log In) Form, Session Management

#### Accounts 

```
 [{ username : 'admin@yahoo.com', password : 'admin' , pri : 'high'},
  { username : 'guest@yahoo.com', password : 'guest' , pri : 'low'}]
```    

#### Sensor Flow 

Sensor Flow is from https://diyprojects.io/node-red-dashboard-gauges-charts-notifications-html

## In Action 

![alt text-1](https://github.com/phyunsj/node-red-dashboard-login/blob/master/dasahboard_session_timeout.gif "Node-RED-Dashboard In Action")


## Flow

![alt text-1](https://github.com/phyunsj/node-red-dashboard-login/blob/master/node-red-dashboard.png "Node-RED-Dashboard Flow")

```
[{"id":"d89c119.f26d4f","type":"function","z":"cd300aa8.60d6f8","name":"Account Verfication","func":"// Accoutn Verification\nvar username = msg.payload.u_name;\nvar password = msg.payload.u_pass;\n\nvar accounts = context.get('accounts')|| [];\n\n// replace with database.\n// default account\n\nif ( accounts.length === 0 ) {\n    accounts.push({ username : 'admin@yahoo.com', password : 'admin' , pri : 'high'});\n    accounts.push({ username : 'guest@yahoo.com', password : 'guest' , pri : 'low'});\n    context.set('accounts', accounts);\n}\n\n// payload = 0 : success\n// payload = 1 : unknwon user\n// payload = 2 : wrong password\nvar msg = {};\nmsg.payload = 1;\n\nfor (var i=0; i < accounts.length; i++) {\n    if (accounts[i].username === username) {\n      \n      if (accounts[i].password === password)  msg.payload = 0;\n      else msg.payload = 2;\n      \n      break;\n    } \n}\n\nif ( msg.payload === 0 ) {\n    flow.set('lastAccessTime', Date.now()  );\n}\nreturn msg;\n","outputs":1,"noerr":0,"x":374.30010986328125,"y":182.66668701171875,"wires":[["ad43eac.e5bf918"]]}]
```

## To-Do-List

- HTTPS Setup (https://www.hardill.me.uk/wordpress/2015/05/11/securing-node-red/) 
- New User Registration
- Database : account, log, etc
