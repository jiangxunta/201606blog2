## 1. 安装项目生成器
```
npm install -g express-generator
```
> 如果安装以后执行express命令报错，则需要把express命令所在的目录添加到环境变量PATH中去
![查看路径](images/menu.jpg)

> 在命令提示符中输入path命令，即可查看当前配置的环境变量

## 2. 生成项目
```
express -e 201606blog
```

## 3. 进入项目目录并安装依赖
```
cd 201606blog && npm install 
```

## 4.启动项目
```
npm start
```

## 5. 配置**.gitignore**文件
```
node_modules 
lib
.idea
```

> 这些文件都不需要提交到github服务器

- node_modules 是npm 安装时依赖的模块
- lib 是我们将要把前端框架如jquery安装的目录
- .idea 是webstorm的配置文件

## 6.路由、文件名、模板等都要去掉s


## 7. 初始化bower
bower 是用来安装前端框架的 bootstrap jquery angular

bower 用途

1. 自动下载对应的软件
2. 自动分析出当前的包依赖的模块，自动安装依赖的模块
3. 可能自行处理版本冲突

```
npm install bower -g

bower init
```

> 初始化完毕后会在当前项目下增加一个`bower.json`配置文件

## 8. 创建bower配置文件
在项目的根目录下创建 .bowerrc 文件,填入以下内容
directory指定下载下来的包(bootstrap)的安装的目录
```
{
  "directory":"./public/lib"
}
```
## 9. 下载bootstrap到lib目录
```
bower install bootstrap --save
```

## 10. 用户注册的功能
1. 编写页面
2. 提交表单的时候要把请求发给后台
3. 后台编写路由来响应请求
4. 响应处理的时候可能会与数据库进行交互

