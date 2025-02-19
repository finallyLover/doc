

# 安装

23778

# 问题

## 将jenkins的shell执行用户改为root

备注：uabntu apt安装方式

```
#进入文件
vi /usr/lib/systemd/system/jenkins.service
#修改配置（将jenkins 改为root 配置位置如下图）

# 重新加载 systemd 的配置文件
systemctl daemon-reload 
# 重启 Jenkins
systemctl restart jenkins 
```

![](/home/ubantu/project/myproject/doc/杂项/jenkins/5a285980fe324834a8b0f29e6df99e69.png)