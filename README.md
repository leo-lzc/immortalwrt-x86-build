# ImmortalWrt x86_64 Build

基于 ImmortalWrt 24.10.6 构建 x86_64 固件。

## 特性

- x86_64
- UEFI
- squashfs
- GPT / combined-efi
- LuCI
- APK 包管理
- Docker
- FRP
- Passwall 2
- DDNSTO
- SmartDNS
- Nikki
- IPv6
- 常见网卡驱动
- Intel i226-V (`igc`)
- Intel 82599ES (`ixgbe`)

## 默认信息

- 地址: http://192.168.1.1
- 地址: http://immortalwrt.lan
- 用户名: root
- 密码: 空

## 构建方法

1. 上传本仓库到 GitHub
2. 打开 Actions
3. 运行 `Build ImmortalWrt x86_64`
4. 编译完成后下载 artifact

## 输出文件

主要输出：

- `*combined-efi.img.gz`

## 刷写示例

```bash
gzip -dc immortalwrt-xxx-combined-efi.img.gz | sudo dd of=/dev/sdX bs=4M status=progress conv=fsync