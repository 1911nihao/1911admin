#### 这里是dev分支
####  文件目录结构
pages  放页面
components 放组件
style 样式
utils 公用的库或插件
router 路由文件
store 全局状态管理
asset 资源目录

#### 预处理语言
less
npm install less less-loader
默认不支持less 需要在 config webpck.config.js 将所有sass 变为less

#### ui框架
antd less
全局引入 线上环境不建议使用 文件过大  建议开发环境使用
按需引入 安装插件 babel-plugin-import 在webpack.config.js里找plugins 在里面添加 ['import',{'libraryName':'antd','style':true}] 本项目的less版本要与antd的less版本相同
npm install antd
全局引入 100
在index.js import '/antd/dist/antd.css'  可以在官网上面找
按需引入

#### 基本配置
1.起别名
在 config webpck.config.js alias  
'style':path.join(__dirname,'../src/style')
这两种都可以
'style':path.resolve(__dirname,'../src/style')
2.服务器代理
proxy:{
      '/hehe':{
        target:'http://www.baidu.com',
        changeOrigin:true,
        pathRewrite:{
          '^/hehe':''
        }
      },
}
....

#### 公有的库
axios 二次封装
路由
react-redux