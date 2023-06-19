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
