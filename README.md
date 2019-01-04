# 简介
- [x] Tiktok观看
- [x] Tiktok登入
- [x] Tiktok点赞
- [x] Tiktok发布
- [ ] Tiktok下载

## 规则
Rule for Surge3:
```
[URL Rewrite]
(?<=&carrier_region=)CN(?=&is_my_cn=1) JP 307

[MITM]
hostname = *.musical.ly, *.snssdk.com, *.tiktokv.com
```

Rule for Quantumult:
```
[REWRITE]
(?<=&carrier_region=)CN(?=&is_my_cn=1) url 307 JP

[MITM]
hostname = *.musical.ly, *.snssdk.com, *.tiktokv.com
```

## 托管
配置链接 `https://github.com/Choler/Surge/raw/master/Tiktok.conf`

## 证书
* 安装根证书：[点击安装](https://raw.githubusercontent.com/Choler/Surge/master/Thor%20SSL%20CA.cer)
* 信任根证书：手机设置-通用-关于本机-证书信任设置 打开

### 必要
* `Rewrite` 和 `MitM` 同时启用

### 去水印
* 需要时打开抓取流量
* 最近的请求中都为缓存视频
* 点击请求链接再点响应 可查看视频内容
* 如需保存点击最下方Export 点击储存视频
* 此时视频就去水印保存到相册
