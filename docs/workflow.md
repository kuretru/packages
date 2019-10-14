# 工作流程

## nginx动态模块

### nginx-module-brotli

1. 更新[ngx_brotli仓库](https://github.com/google/ngx_brotli)，以及[brotli模块](https://github.com/google/brotli)
2. 复制到新的目录，重命名为`ngx_brotli-{nginx_version}-1`
3. 删除`brotli模块`中，无用且占用空间大的目录{java, research, tests}
4. 将目录打包，生成`ngx_brotli-{nginx_version}-1.tar.gz`
5. 复制到`~/rpmbuild/SOURCES`目录下，并在该目录下下载新版本[nginx源码](http://nginx.org/en/download.html)
6. 下载新版本`nginx-module-deoip.src`包，安装包并提取`.spec`变更
7. 将变更加入至`nginx-module-brotli.spec`，并添加`changelog`
8. `rpmbuild -ba`重新编译
9. 复制生成的包至包仓库并发布
