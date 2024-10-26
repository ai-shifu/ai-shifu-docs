# 部署及调试


## 复制代码到本地

```bash
git clone https://github.com/ai-shifu/ai-shifu.git
```

## 进入代码中的Docker目录

```bash
cd ai-shifu/docker  
```

## 复制.env.example文件为.env

```bash
cp .env.example .env
```

## 更改环境变量

系统的详细环境变量配置具体可以参考[环境变量配置](./environment-variables.md)章节

但其中最重要的为`LARK_APP_ID`和`LARK_APP_SECRET`，请参考[飞书应用的准备及配置](preparation.md)章节，打开.env文件，将其改为你的飞书应用的ID和Secret


```bash
LARK_APP_ID=your_lark_app_id
LARK_APP_SECRET=your_lark_app_secret
```

## 准备至少一个大模型配置   

请参考[模型配置](../configuration/models-and-configurations.md) 及[环境变量配置](../environment-variables.md)，准备至少一个大模型配置


## 启动系统
在docker目录下，执行启动命令

```bash
docker compose up -d
```

成功启动后,可看到如下输出
 

<img src="../img/zh-deployment-docker-start-success.png" alt="">

## 配置

系统启动后，可以通过`http://localhost:8081` 访问系统，进入Cook配置页面

系统的默认用户: `ai-shifu`，默认密码: `AIshifu@2024`

## 运行课程
在Cook配置好您的课程后，可以通过`http://localhost:8080` 访问课程页面,进行课程的运行



## 调试

我们提供了本地编译&运行的脚本，具体方式为：

在配置好环境变量后，执行`docker` 下的`dev_in_docker.sh` 脚本，即可启动本地编译&运行环境

```bash
./dev_in_docker.sh
```

