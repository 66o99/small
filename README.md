


#### 使用


编译固件一键命令
```yaml

sed -i '$a src-git kenzo https://github.com/66o99/openwrt-packages' feeds.conf.default
sed -i '$a src-git small https://github.com/66o99/small' feeds.conf.default

#git pull 无效命令

./scripts/feeds update -a
./scripts/feeds install -a
make menuconfig
```

单独编译IPK插件
```yaml
在已经跑过一边的机器上，进入到 /package 目录下

//拉取插件包
git clone https://github.com/66o99/openwrt-packages.git
//拉取依赖包
git clone https://github.com/66o99/small.git
//选择要编译的插件
make menuconfig  > 选中<M>不编译进固件！
//开始编译
make package/luci-app-ssr-plus/compile v=99
```

- openwrt 固件编译自定义主题与软件

| 软件名                       | 说明                   | 中文说明    |
| -----------------------------|------------------------| ------------|
| luci-app-vssr                | vssr proxy                 | vssr老竭力代理软件        |
| luci-app-dnsfilter           | dns ad filtering            | 基于DNS的广告过滤        |
| luci-app-openclash           | openclash proxy            |  clash的图形代理软件      |
| luci-app-advanced            | System advanced settings               | 系统高级设置        |
| luci-app-pushbot             | WeChat/DingTalk Pushed plugins    |   微信/钉钉推送        |
| luci-theme-atmaterial_new    | atmaterial theme (adapted to luci-18.06) | Atmaterial 三合一主题        |
| luci-app-aliddns             | aliyunddns         |   阿里云ddns插件      |
| luci-app-eqos                | Speed ​​limit by IP address       | 依IP地址限速      |
| luci-app-gost                | https proxy      | 隐蔽的https代理   |
| luci-app-adguardhome         | Block ads          |  AdG去广告      |
| luci-app-smartdns            | smartdns dns pollution prevention     |  smartdns DNS防污染       |
| luci-app-passwall            | passwall proxy      | passwall代理软件        |
| luci-theme-argonne           | argonne theme           | 修改老竭力主题名     |
| luci-app-argonne-config      | argonne theme settings            |  argonne主题设置      |
| luci-app-ssr-plus            | ssr-plus proxy              | ssr-plus 代理软件       |
| luci-theme-mcat              | Modify topic name          |   mcat主题        |
| luci-theme-tomato            | Modify topic name             |  tomato主题        |
| luci-theme-neobird           | neobird theme          | neobird主题        |
| luci-app-mosdns              | mosdns dns offload            |DNS 国内外分流解析与广告过滤        |
| luci-app-store               | store software repository            |  应用商店   |
| luci-app-unblockneteasemusic | Unlock NetEase Cloud Music         | 解锁网易云音乐   |
| luci-app-aliyundrive-webdav  | Aliyun Disk WebDAV Service            |  阿里云盘 WebDAV 服务   |
| luci-app-amlogic  | Amlogic Service             |  晶晨宝盒   |

