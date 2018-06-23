# Node-RED-Dashboard : Log-In, Session

Node-RED Dashboard Example with Sign In (Log In) Form, Session Management

#### Accounts 

```
 [{ username : 'admin@yahoo.com', password : 'admin' , pri : 'high'},
  { username : 'guest@yahoo.com', password : 'guest' , pri : 'low'}]
```    

#### Sensor Flow 

The Sensor Flow (and modified for this demo) is from https://diyprojects.io/node-red-dashboard-gauges-charts-notifications-html

#### `ui-control`

  
- Transition from `Login` to `Measurement` & `Graph` Group.  ( `TabName`_`GroupName` )

 > `{group:{hide:["Dashboard_Login"], show:["Dashboard_Graph", "Dashboard_Measurement"], focus:true}} `

- Transition from `Measurement` & `Graph` Group to `Login` Group.

 > `{group:{hide:["Dashboard_Graph","Dashboard_Measurement"], show:["Dashboard_Login"], focus:true}}`

## In Action 


<p align="center">
<img src="https://github.com/phyunsj/node-red-dashboard-login/blob/master/dasahboard_session_timeout.gif" width="600px"/>
</p>

## Flow

<p align="center">
<img src="https://github.com/phyunsj/node-red-dashboard-login/blob/master/node-red-dashboard.png" width="600px"/>
</p>


## To-Do-List

- HTTPS Setup (https://www.hardill.me.uk/wordpress/2015/05/11/securing-node-red/) 
- New User Registration
- Database : account, log, etc

