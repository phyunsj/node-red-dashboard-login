# Node-RED-Dashboard : Log-In, Session Management

Node-RED Dashboard Example with Sign In (Log In) Form, Session Management

#### Accounts 

```
 [{ username : 'admin', password : 'admin' },
  { username : 'guest', password : 'guest' }]
```    

#### Sensor Flow 

The Sensor Flow (and modified for this demo) is from https://diyprojects.io/node-red-dashboard-gauges-charts-notifications-html

#### `ui-control`

  
- Transition from `Login` to `Measurement` & `Graph` Group.  ( `TabName`_`GroupName` )

 > `{group:{hide:["Dashboard_Signin"], show:["Dashboard_SensorData", "Dashboard_History"], focus:true}} `

- Transition from `Measurement` & `Graph` Group to `Login` Group.

 > `{group:{hide:["Dashboard_SensorData","Dashboard_history"], show:["Dashboard_Signin"], focus:true}}`

<p align="center">
<img src="https://github.com/phyunsj/node-red-dashboard-login/blob/master/node-red-dashboard-session-layout.png" width="300px"/>
</p>

## In Action 


<p align="center">
<img src="https://github.com/phyunsj/node-red-dashboard-login/blob/master/node-red-dashboard-session-action.gif" width="600px"/>
</p>

## Flow

<p align="center">
<img src="https://github.com/phyunsj/node-red-dashboard-login/blob/master/node-red-dashboard-session-flow.png" width="600px"/>
</p>


## Additional Development

- HTTPS Setup (https://www.hardill.me.uk/wordpress/2015/05/11/securing-node-red/) 
- New User Registration
- Database : account, log, etc

