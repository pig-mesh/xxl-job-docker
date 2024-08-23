# XXL-Job Docker 项目

本项目提供了基于 Docker 的 XXL-Job 快速部署方案，使用简单，方便快速启动 XXL-Job 管理平台。

## 使用方法

### 1. 下载源码

使用以下命令克隆项目源码：

```shell
git clone https://github.com/pig-mesh/xxl-job-docker.git
```

### 2. 使用 Docker Compose 运行

#### 2.1 默认设置

在 `docker-compose.yml` 文件中，默认绑定宿主机端口为 `38080`，可以根据需要自行修改。

#### 2.2 启动服务

在项目根目录下执行以下命令启动服务：

```bash
docker compose up -d
```

### 3. 访问 XXL-Job 管理平台

服务启动成功后，您可以通过以下地址访问 XXL-Job 管理平台：

```
http://localhost:38080/xxl-job-admin
```

### 4. 停止服务

如需停止服务，可以执行以下命令：

```bash
docker compose down
```

## 常见问题

### 如何修改端口？

如果需要修改绑定的宿主机端口，可以编辑 `docker-compose.yml` 文件，找到以下内容：

```yaml
ports:
  - "38080:8080"
```

将 `38080` 修改为您想要的端口号。

### 如何查看日志？

您可以通过以下命令查看容器日志：

```bash
docker logs -f <容器名称>
```

容器名称可以通过 `docker ps` 命令查看。

### 如何重启服务？

执行以下命令可以重启服务：

```bash
docker compose restart
```

## 相关链接

- XXL-Job 官方文档：[https://www.xuxueli.com/xxl-job](https://www.xuxueli.com/xxl-job)
- 项目 GitHub 仓库：[https://github.com/pig-mesh/xxl-job-docker](https://github.com/pig-mesh/xxl-job-docker)

