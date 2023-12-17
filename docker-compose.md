视频中用到的命令及地址
设置环境变量
DOCKER_CONFIG=${DOCKER_CONFIG:-$HOME/.docker}
建立插件目录
mkdir -p $DOCKER_CONFIG/cli-plugins
下载二进制文件
$ curl -SL https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64 -o $DOCKER_CONFIG/cli-plugins/docker-compose
赋予权限
chmod +x $DOCKER_CONFIG/cli-plugins/docker-compose
验证命令：
docker compose version

dockge github页面
https://github.com/louislam/dockge
mkdir -p /opt/stacks /opt/dockge
下载配置文件：
curl "https://dockge.kuma.pet/compose.yaml?port=5001&stacksPath=/opt/stacks" --output compose.yaml
启动容器
docker compose up -d
