# Docker常用命令

很多时候我们起了很多个docker镜像，或者使用docker compose起了很多个镜像，停止，重启，删除的时候却要一个一个的操作容器ID来停止或者重启。这些命令覆盖了从镜像操作到容器管理的基本操作：

## 镜像操作
**拉取镜像**:

   ```bash
   docker pull [镜像名]:[标签]
   ```
**查看本地镜像**:
   ```bash
   docker images
   ```
**构建镜像**:
   ```bash
   docker build -t [镜像名]:[标签] [Dockerfile路径]
   ```
**删除镜像**:
   ```bash
   docker rmi [镜像ID或名称]
   ```
## 容器操作
**运行容器**:
   ```bash
   docker run [选项] [镜像名]:[标签] [命令]
   ```
**查看运行中的容器**:
   ```bash
   docker ps
   ```
**查看所有容器（包括未运行的）**:
   ```bash
   docker ps -a
   ```
**停止容器**:
   ```bash
   docker stop [容器ID或名称]
   ```
**启动容器**:
   ```bash
   docker start [容器ID或名称]
   ```
**重启容器**:
   ```bash
   docker restart [容器ID或名称]
   ```
**进入容器**:
   ```bash
   docker exec -it [容器ID或名称] [命令]
   ```
**删除容器**:
   ```bash
   docker rm [容器ID或名称]
   ```
**查看容器日志**:
   ```bash
   docker logs [容器ID或名称]
   ```
**查看容器详细信息**:
    ```bash
    docker inspect [容器ID或名称]
    ```
## 容器与主机之间的数据卷操作
**挂载宿主机目录到容器**:
   ```bash
   docker run -v [宿主机路径]:[容器路径] [镜像名]:[标签] [命令]
   ```
**查看数据卷**:
   ```bash
   docker volume ls
   ```
**删除数据卷**:
   ```bash
   docker volume rm [数据卷名称]
   ```
## 网络操作
**查看网络**:
   ```bash
   docker network ls
   ```

**连接容器到网络**:
   ```bash
   docker network connect [网络名称] [容器ID或名称]
   ```

**断开容器与网络的连接**:
   ```bash
   docker network disconnect [网络名称] [容器ID或名称]
   ```
   这些命令是Docker日常使用中非常基础和重要的部分，掌握它们可以帮助你更有效地管理和操作Docker容器和镜像。