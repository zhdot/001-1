
[![Deploy](https://www.herokucdn.com/deploy/button.png)](https://dashboard.heroku.com/new?template=https://github.com/zhdot/001-1)

### 路径

`WebSocket` 路径(配置文件中的 `path` )为 `/` 。

### 端口

`端口` 为 `443` 。

### UUID

`UUID` 默认为 `24b4b1e1-7a89-45f6-858c-242cf53b5bdb` 可自行设置。

## 流量中转

<details>
<summary>可以使用cloudflare的workers来中转流量，配置为：  </summary>

```js
addEventListener(  
    "fetch",event => {  
        let url=new URL(event.request.url);  
        url.hostname="xxx.herokuapp.com";//你的heroku域名    
        let request=new Request(url,event.request);  
        event. respondWith(  
            fetch(request)  
        )  
    }  
)  
```
</details>

## OpenWrt优选IP脚本自动更新：

* [CloudflareST](https://github.com/Lbingyi/CloudflareST) `OpenWrt推荐-速度较快`
* [cf-autoupdate](https://github.com/Lbingyi/cf-autoupdate) `OpenWrt推荐`

## 关于CF筛选IP

* 请参考 [CloudflareSpeedTest](https://github.com/XIU2/CloudflareSpeedTest) `推荐`
* 请参考 [better-cloudflare-ip](https://github.com/badafans/better-cloudflare-ip)

### 特别感谢 ：

* [bclswl0827](https://github.com/bclswl0827/v2ray-heroku)
* [yxhit](https://github.com/yxhit)
* [badafans](https://github.com/badafans/better-cloudflare-ip/tree/20201208)
