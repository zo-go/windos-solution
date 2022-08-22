让 systemd 在执行 ExecStart 的指令后等待一点点时间即可
如果你的 nginx 启动需要时间更长，可以把 sleep 时间改长一点
建立目录
mkdir -p /etc/systemd/system/nginx.service.d

在新建目录中建立文件override.conf，输入内容

[Service]
ExecStartPost=/bin/sleep 0.1
然后
systemctl daemon-reload
systemctl restart nginx.service