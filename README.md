# TikTok
This is a sample configuration file:

```
[Rule]
DOMAIN,api-h2.tiktokv.com,PROXY

[URL Rewrite]
(.*video_id=\w{32})(.*watermark=)(.*) $1 302
(?<=(carrier|account|sys)_region=)CN JP 307

[MITM]
hostname = api*.tiktokv.com
ca-passphrase = 123456
ca-p12 = MIIKKgIBAzCCCfQGCSqGSIb3DQ…
```
