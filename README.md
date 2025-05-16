# Buildroot 水下机器人实验室定制

基于 `board\friendlyarm\nanopi-neo` 编辑

- 更改终端为 zsh
- 添加 openssh
- 添加 root 密码为 “password”
- 以太网静态 ip “192.168.137.219”
- 添加 libev、i2c-tools、libgpiod
- 修改设备树，启用 uart 0 ~ 3，i2c 0 ~ 2，spi0