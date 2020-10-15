# step 1: 安装必要的一些系统工具
    sudo yum install -y yum-utils device-mapper-persistent-data lvm2
# Step 2: 添加软件源信息
    sudo yum-config-manager --add-repo http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo
# Step 3: 更新并安装 Docker-CE
    sudo yum makecache
    sudo yum -y install docker-ce
    查看docker历史版本
    yum list docker-ce.x86_64 --showduplicates | sort -r
# Step 4: 开启Docker服务
    sudo systemctl enable docker
    sudo s**ystemctl start docker