<h1 align="center">
  <img src="https://i.loli.net/2019/01/06/5c315fe70c2b7.jpg" alt="TikTok" width="88">
</h1>

# 简介
`Rewrite` 和 `MitM` 同时启用，规则方能生效！

## 规则
Rule for Surge3:
```
[URL Rewrite]
(.*video_id=\w{32})(.*watermark=)(.*) $1 302
(?<=(carrier|account|sys)_region=)CN JP 307

[MITM]
hostname = api*.tiktokv.com
```

Rule for Quantumult:
```
[REWRITE]
(.*video_id=\w{32})(.*watermark=)(.*) url 302 $1
(?<=(carrier|account|sys)_region=)CN url 307 JP

[MITM]
hostname = api*.tiktokv.com
```

## 托管
[配置文件](https://github.com/Choler/TikTok/raw/master/TikTok.conf) `https://github.com/Choler/TikTok/raw/master/TikTok.conf`   

* 安装根证书：[点击安装](https://raw.githubusercontent.com/Choler/TikTok/master/Thor%20SSL%20CA.cer) (Thor SSL CA 18-05-20 13:14)
* 信任根证书：设置-通用-关于本机-证书信任设置-针对根证书启用完全信任

### 去水印
* 需要时打开`抓取流量`开关
* 在`最近的请求`中都为缓存视频
* 点击请求链接再点`响应`可查看视频内容
* 如需保存点击最下方`导出`储存视频到相册
