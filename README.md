<h1 align="center">
  <img src="https://i.loli.net/2019/01/06/5c315fe70c2b7.jpg" alt="TikTok" width="99">
</h1>

# 简介
`api*.tiktokv.com` 兼容TikTok ，`api*.musical.ly` 兼容美区TikTok     
`api*.amemv.com` `aweme*.snssdk.com` 抖音短视频去水印下载   
  
## 下载超时
`DOMAIN-SUFFIX,tiktokv.com,Proxy`   
`DOMAIN-SUFFIX,musical.ly,Proxy`

## 规则
Rule for Surge3:
```
[URL Rewrite]
(.*video_id=\w{32})(.*watermark=)(.*) $1 302
(?<=(carrier|account|sys)_region=)CN JP 307
```

Rule for Quantumult:
```
[REWRITE]
(.*video_id=\w{32})(.*watermark=)(.*) url 302 $1
(?<=(carrier|account|sys)_region=)CN url 307 JP

```

## 托管
[配置文件](https://github.com/Choler/TikTok/raw/master/TikTok.conf) `https://github.com/Choler/TikTok/raw/master/TikTok.conf`   

* 安装根证书：[点击安装](https://raw.githubusercontent.com/Choler/TikTok/master/Thor%20SSL%20CA.cer) (Thor SSL CA 18-05-20 13:14)
* 信任根证书：设置-通用-关于本机-证书信任设置-针对根证书启用完全信任
