### 该插件用于辅助api调用时无法识别类型的问题,当然这个插件只是针对金农的微前端项目

#### 安装

```bash
pnpm add @jsjn/inject-api-type

// 这个是必须的,插件内使用了ts-morph来解析ts文件
pnpm add ts-morph
```

#### 使用

在要使用的项目目录下的vue.config.js中添加如下配置

```js
const InjectApiType = require('@jsjn/inject-api-type')
module.exports = defineConfig({
  configureWebpack: {
    plugins: [
      new InjectApiType()
    ]
  }
})
```

> 注意: vue.config.js同级的tsconfig.json中不能有注释内容,否则会导致项目运行时报错

![image](https://s1.imagehub.cc/images/2025/01/20/5d612b03a067af801c4e495eba01dedb.png)

#### 效果

模块名
![image](https://s1.imagehub.cc/images/2025/01/20/8652347f88e2a0d2092230061263ef3d.png)

模块下所有的接口
![image](https://s1.imagehub.cc/images/2025/01/20/58a712f2f9698e7fdd92c44132180a11.png)
