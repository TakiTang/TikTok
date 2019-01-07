<h1 align="center">
  <img src="https://i.loli.net/2019/01/06/5c315fe70c2b7.jpg" alt="TikTok" width="88">
</h1>

# 简介
`Rewrite` 和 `MitM` 同时启用，规则方能生效！
- [x] Tiktok观看
- [x] Tiktok登入
- [x] Tiktok点赞
- [x] Tiktok发布
- [x] Tiktok下载
- [x] Tiktok评论

## 规则
Rule for Surge3:
```
[URL Rewrite]
(?<=&carrier_region=)CN(?=&is_my_cn=1) JP 307

[MITM]
hostname = *.tiktokv.com, *.musical.ly
```

Rule for Quantumult:
```
[REWRITE]
(?<=&carrier_region=)CN(?=&is_my_cn=1) url 307 JP

[MITM]
hostname = *.tiktokv.com, *.musical.ly
```

## 托管
配置链接 `https://github.com/Choler/Surge/raw/master/Tiktok.conf`

## 证书
* 安装根证书：[点击安装](https://raw.githubusercontent.com/Choler/Surge/master/Thor%20SSL%20CA.cer) (Thor SSL CA 18-05-20 13:14)
* 信任根证书：手机设置-通用-关于本机-证书信任设置-针对根证书启用完全信任

### 去水印
* 需要时打开`抓取流量`
* 在`最近的请求`中都为缓存视频
* 点击请求链接再点`响应`可查看视频内容
* 如需保存点击最下方`导出`储存视频到相册
