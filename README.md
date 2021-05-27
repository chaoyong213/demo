### demo 测试静态资源

>利用jsdelivr+github使用免费又好用的全球节点CDN

>什么是jsDelivr

>官网地址：https://www.jsdelivr.com/

>jsdelivr的格式是 https://cdn.jsdelivr.net/gh/chaoyong213/demo/jquery-1.8.3.js

```
其中user代表用户名，我的是chaoyong213
repo代表项目名，就是刚才创建项目名：demo
version代表的是版本号或者分支号，就是刚才创建的版本：1.0.0（可省略）
file代表的是文件路径，我的是在根目录的：jquery.min.js
最终组成：https://cdn.jsdelivr.net/gh/chaoyong213/demo@1.0.0/jquery-1.8.3.js
或者不区分版本：https://cdn.jsdelivr.net/gh/chaoyong213/demo/jquery-1.8.3.js
```
>将“ .min”添加到任何JS / CSS文件以获取缩小版本，不存在将会自动生成，第一次会访问慢，接下来访问就是生成好的了

>在末尾添加/以获取目录列表，如https://cdn.jsdelivr.net/gh/chaoyong213/demo@1.0.0/

### 缓存更新
有时候更改文件没有及时生效，对于 jsDelivr，缓存刷新的方式也很简单，只需将想刷新的链接的开头的cdn 更改为 purge，不过官网说后面会推出刷新工具，我这边还在观望中
https://cdn.jsdelivr.net/
切换为
https://purge.jsdelivr.net/
返回status: ok，就代表完成了
```
{
  "success": true,
  "error": null,
  "paths": [
    "gh/chaoyong213/demo/jquery-1.8.3.js"
  ],
  "cdn": {
    "fastly": true,
    "bunny": true,
    "cloudflare": true,
    "quantil": true
  }
}
```

### 注意事项
单文件大小不得大于20M,音视频媒体如视频都是不支持的。
