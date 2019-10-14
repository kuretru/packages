# packages

呉真自编译RPM包仓库

## 操作系统支持

* [ ] CentOS 6(i386, x86_64)
* [x] CentOS 7(x86_64)
* [ ] CentOS 8(x86_64)

## 使用方法

```bash
wget http://kuretru.github.io/packages/kuretru.repo -O /etc/yum.repos.d/kuretru.repo
```

## 包列表

### nginx-module-brotli

为使用[Nginx官方源](https://nginx.org/en/linux_packages.html)安装的Nginx添加Brotli动态模块，以开启Brotli新一代压缩算法支持。
