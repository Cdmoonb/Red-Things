# Red-Things
IOT(Internet of things) platform based on Node-Red, Easy but very useful to built iot system

Red-Things项目意义:基于Node-Red技术,快速构建一个简单好用的物联网平台.

# Init project
> npm install

# Install views JS lib
```
cd public
npm install
```

why? 

Important pages render in backend;

And login.html is all pages's entry;

There will be different Vue projects in Red-Things in the future;


# Config DB
only support mongoDB

dir /user_settings/index.js  ->  db_url

input your own mongoDB server address

# Start to run
> npm run server

# Create admin account
input below command in terminal:
> node utils/createUser.js username password

or

```
cd utils
node createUser.js username password
```
+ username : your own account name
+ password : your own password

# Test
input url in browser: localhost:3000/login

you will see the login page

![login](http://www.v5w.com/wp-content/uploads/2020/04/1587838198-d56b699830e77ba.png)

# Interface
+ /login  all url's entry
+ /admin  admin url
+ /client client url
+ /red    node-red editor
+ /api    node-red http interface

# RedFunction
define yourself function,and export it;

you can use global.get('function name') to get the function in node-red, then you can use it!

example:
```
//testFun.js
module.exports=function(){
    console.log('test function is running-----------');
}

//export module
// RedFunction/index.js
module.exports={
    testFun
}

//in node-red
//get it
const testFun= global.get('testFun');
//use it
testFun();
```



# www.v5w.com
more information in my website(威武网): 

https://www.v5w.com

demonstrate video(演示视频):

https://www.v5w.com/iot/259.html