<img align="left" width="80" height="80" src="app/src/main/res/mipmap-xxxhdpi/ic_launcher.webp"
alt="App icon">

# WebDAV Provider [![build](https://github.com/alexbakker/webdav-provider/actions/workflows/build.yaml/badge.svg)](https://github.com/alexbakker/webdav-provider/actions/workflows/build.yaml)

__WebDAV Provider__ 是一款能够通过安卓存储访问框架（SAF）暴露WebDAV服务的安卓应用。这使您可以通过安卓内置的文件管理器以及设备上的其他应用来访问您的WebDAV存储空间。

[<img height=80 alt="Get it on Google Play"
src="https://play.google.com/intl/en_us/badges/images/generic/en-play-badge.png"
/>](https://play.google.com/store/apps/details?id=dev.rocli.android.webdav)

## Screenshots

[<img src="screenshots/screenshot1.png"
width="200">](screenshots/screenshot1.png) [<img
src="screenshots/screenshot2.png" width="200">](screenshots/screenshot2.png)
[<img src="screenshots/screenshot3.png"
width="200">](screenshots/screenshot3.png) [<img
src="screenshots/screenshot4.png" width="200">](screenshots/screenshot4.png)

## Development

本项目已针对多种不同的WebDAV服务器进行自动化测试。测试在Android模拟器中运行，并连接到宿主机上独立容器中运行的WebDAV服务器。
启动测试环境的步骤如下：

```sh
docker compose --project-directory tests up -d --wait --force-recreate --build --renew-anon-volumes --remove-orphans
```

假设安卓模拟器正在运行，请使用以下命令来运行测试：

```sh
./gradlew connectedCheck
```

关闭测试环境：

```sh
docker compose --project-directory tests down -v
```
