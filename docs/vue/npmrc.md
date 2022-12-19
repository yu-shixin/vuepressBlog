# .npmrc 文件的作用

有些项目根目录下可能有个. npmrc 的文件，点开一看只有一句话  

registry=[http://registry.npm.xxxx.com](https://links.jianshu.com/go?to=http%3A%2F%2Fregistry.npm.xxxx.com) 

就是 npm 仓库镜像地址

在 npm i 的时候，如果项目根目录下有这个文件，会自动从这个镜像地址下安装 node_modules，不需要手动设置镜像地址

