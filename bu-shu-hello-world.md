### 创建和部署hello world {#articleHeader5}

以root用户身份在根目录下创建www目录,www目录下创建hello文件夹,里面就一个文件，hello.js,内容如下：

```javascript
const http = require('http')
http.createServer(function(req,res) {
res.writeHead(200,{'Content-Type':'text/plain'})
res.end('hello world')
}).listen(8081)

console.log('server test')
```

以上是一个最简单的node服务，服务输出hello world，我们要让它在服务器上跑起来，要用到pm2

pm2的几个常用命令：

* pm2 start preject   启动项目

* pm2 list 查看启动的应用

* pm2 show preject   查看详细信息

* pm2 logs 查看当前信息

* pm2 stop preject  停止preject

* pm2 delete preject 删除preject

#### 启动服务

执行pm2 start hello你的服务就跑起来了，此时地址栏输入http://198.10.10.100:8081（你自己的服务器IP）就会看到hello world

执行pm2 list回看到详细信息

![](/assets/2017-12-01_174154.png)


