###云  API
***
了解 APICloud平台提供的数据通信能力，掌握  APICloud数据通信相关  API 使用，按照服务端接口文档进行 APP 前后端接口联调，将  APP 页面中的静态数据改为从服务端动态获取，并完成相关的业务逻辑。了解  APICloud数据云功能和使用。
###[课程视频]()：
完成[登录 、注册](https://pan.baidu.com/s/1eS5gxVW)、 [信息列表动态获取](https://pan.baidu.com/s/1nvpsZPZ)。
***
##课程大纲
***
1. 按照服务端接口文档，进行  APP 与服务端的接口联调  
var model = api.require('model');  
model.config({  
    appId:'A123456789',  
    appKey: 'A991A337-0212-A29D-0C9C-A518E39FXXXX',  
    host: 'https://d.apicloud.com'  
}); 
2. 登录、注册  
var user = api.require('user');  
user.login({  
    username: 'name',  
    password: '12345678'  
}, function( ret, err ) {  
     if( ret ){  
        alert( JSON.stringify( ret) );  
     }else{  
        alert( JSON.stringify( err) );  
     }  
});  

var user = api.require('user');  
user.register({  
    username: 'uname',  
    password: '111111',  
    email: 'xixi@apicloud.com'  
}, function( ret, err ) {  
    if( ret ){  
        alert( JSON.stringify( ret) );  
    }else{  
        alert( JSON.stringify( err) );  
    }  
});  
3. 信息列表获取  
var model = api.require('model');  
model.findAll({  
    class: "activity",  
    qid: queryId  
}, function( ret, err ) {  
    if( ret ){  
         alert( JSON.stringify( ret ) );  
    }else{  
         alert( JSON.stringify( err ) );  
    }  
});  