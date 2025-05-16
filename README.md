# Buildroot 水下机器人实验室定制

基于 `board\friendlyarm\nanopi-neo` 编辑

- 更改终端为 zsh
- 添加 openssh
- 添加 root 密码为 “password”
- 以太网静态 ip “192.168.137.219”
- 添加 libev、i2c-tools、libgpiod
- 修改设备树，启用 uart 0 ~ 3，i2c 0 ~ 2，spi0

使用指南参考 Buildroot 官方教程

编译命令

```shell
# 安装依赖
sudo apt update && sudo apt install build-essential cpio unzip libncurses5-dev libncursesw5-dev

# 应用配置 && 下载源代码 && 编译
make friendlyarm_nanopi_neo_defconfig && make source && make
```

编译完成的镜像在 `output/images/sdcard.img` ，output 目录下一并有交叉编译器