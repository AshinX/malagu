# 应用配置

应用配置的结构和组件配置是一样的，也分为前后端独享和共享属性。在项目构建期间，会将所有的组件配置和应用配置进行合并，形成最终的应用配置，在代码中可以通过 @value 注解注入想要的属性配置。

## 多环境的支持

框架默认加载项目根目录下面的 `app.yml` 作为应用配置，该配置不区分环境，默认都会加载，如果你需要加载特定环境下的应用配置，你可以在 `app.yml` 中添加一个 `mode: test` 属性，然后在项目根目录新建一个 `app-test.yml` 文件，框架就会加载该属性文件，属性优先级比 `app.yml` 高。