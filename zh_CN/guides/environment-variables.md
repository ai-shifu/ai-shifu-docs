# 环境变量配置

## 环境变量文件

环境变量文件为`docker/.env`，具体配置可以参考`.env.example`文件

## API 服务环境变量说明

### 基础配置

#### FLASK_APP

Flask应用的入口文件，默认值为`app.py`

#### RESET_PWD_CODE_EXPIRE_TIME

重置密码验证码过期时间，默认值为`300`秒

#### CAPTCHA_CODE_EXPIRE_TIME

验证码过期时间，默认值为`300`秒

#### PHONE_CODE_EXPIRE_TIME

手机验证码过期时间，默认值为`300`秒

#### PHONE_EXPIRE_TIME

手机验证码有效时间，默认值为`1800`秒

#### LOGGING_PATH

日志文件路径，默认值为`/var/log/ai-asistant.log`

### MYSQL 配置

#### SQLALCHEMY_DATABASE_URI

MySQL数据库URI，默认值为`mysql://root:ai-shifu@ai-shifu-mysql:3306/ai-shifu`

**注意**：如果需要使用Docker部署，请使用默认值，如果需要使用本地MySQL，请修改为本地MySQL的URI

#### SQLALCHEMY_POOL_SIZE

MySQL连接池大小，默认值为`20`

#### SQLALCHEMY_POOL_TIMEOUT

MySQL连接池超时时间，默认值为`30`秒

#### SQLALCHEMY_POOL_RECYCLE

MySQL连接池回收时间，默认值为`3600`秒

#### SQLALCHEMY_MAX_OVERFLOW

MySQL连接池最大溢出数，默认值为`20`

### REDIS 配置

#### REDIS_HOST

Redis主机，默认值为`ai-shifu-redis`

**注意**：如果需要使用Docker部署，请使用默认值，如果需要使用本地Redis，请修改为本地Redis的URI

#### REDIS_PORT

Redis端口，默认值为`6379`
#### REDIS_DB

Redis数据库，默认值为`0`

#### REDIS_PASSWORD

Redis密码，默认值为`""`

#### REDIS_USER

Redis用户，默认值为`""`

#### REDIS_KEY_PRRFIX

Redis键前缀，默认值为`ai-shifu:`

#### REDIS_KEY_PRRFIX_USER

用户键前缀，默认值为`ai-shifu:user:`

#### REDIS_KEY_PRRFIX_RESET_PWD

重置密码键前缀，默认值为`ai-shifu:reset_pwd:`

#### REDIS_KEY_PRRFIX_CAPTCHA

验证码键前缀，默认值为`ai-shifu:captcha:`

#### REDIS_KEY_PRRFIX_PHONE

手机键前缀，默认值为`ai-shifu:phone:`

#### REDIS_KEY_PRRFIX_PHONE_CODE

手机验证码键前缀，默认值为`ai-shifu:phone_code:`

### JWT 配置

#### JWT_KEY

JWT密钥，默认值为`ai-shifu`

#### TOKEN_EXPIRE_TIME

JWT过期时间，默认值为`604800`秒

#### SECRET_KEY

SECRET_KEY，默认值为`ai-shifu`

### 阿里云短信配置

#### ALIBABA_CLOUD_ACCESS_KEY_ID

阿里云AccessKey ID 

#### ALIBABA_CLOUD_ACCESS_KEY_SECRET

阿里云AccessKey Secret 

#### ALIBABA_CLOUD_SMS_SIGN_NAME

阿里云短信签名

#### ALIBABA_CLOUD_SMS_TEMPLATE_CODE

阿里云短信模板Code

### Langfuse 配置


#### LANGFUSE_PUBLIC_KEY

Langfuse公钥

#### LANGFUSE_SECRET_KEY

Langfuse密钥

#### LANGFUSE_HOST

Langfuse地址


### 大模型相关配置

#### OPENAI_BASE_URL

OpenAI地址

#### OPENAI_API_KEY

OpenAI API Key

#### ERNIE_API_ID

Baidu 千帆平台 ERNIE API ID

#### ERNIE_API_SECRET

Baidu 千帆平台 ERNIE API Secret

#### BIGMODEL_API_KEY

智谱 AI BigModel API Key
        
#### DEEP_SEEK_API_KEY

DeepSeek API Key

#### DEEP_SEEK_API_URL

DeepSeek API URL，默认值为`https://api.deepseek.com`

#### QWEN_API_KEY

阿里千问的 API Key

#### QWEN_API_URL

Qwen API URL，默认值为`https://dashscope.aliyuncs.com/compatible-mode/v1`


## 前端服务环境变量说明

### 基础配置

#### REACT_APP_BASEURL

API 服务地址

#### REACT_APP_COURSE_ID

默认课程ID

#### REACT_APP_ALWAYS_SHOW_LESSON_TREE

是否总是在左侧显示课程树，默认值为`true`

#### REACT_APP_APP_ID

微信应用ID

#### REACT_APP_ERUDA

是否启用Eruda，默认值为`true`

#### REACT_APP_UMAMI_WEBSITE_ID

Umami网站ID

#### REACT_APP_UMAMI_SCRIPT_SRC

Umami脚本源

#### PORT

端口，默认值为`5000`


## Cook 服务环境变量说明


#### COOK_DB_USERNAME

Cook数据库用户名，默认值为`root`

**注意**：如果需要使用Docker部署，请使用默认值，如果需要使用本地MySQL，请修改为本地MySQL的用户名

#### COOK_DB_PASSWORD

Cook数据库密码，默认值为`ai-shifu`

**注意**：如果需要使用Docker部署，请使用默认值，如果需要使用本地MySQL，请修改为本地MySQL的密码

#### COOK_DB_DATABASE

Cook数据库名称，默认值为`ai-shifu-cook`

**注意**：如果需要使用Docker部署，请使用默认值，如果需要使用本地MySQL，请修改为本地MySQL的数据库名称

#### COOK_DB_HOST

Cook数据库主机，默认值为`ai-shifu-mysql`

**注意**：如果需要使用Docker部署，请使用默认值，如果需要使用本地MySQL，请修改为本地MySQL的主机

#### COOK_IMG_LOCAL_DIR

Cook图片本地目录，默认值为`/data/img/`

#### COOK_IMG_OSS_ANAME

Cook图片OSS名称

#### COOK_IMG_OSS_ENDPOINT

Cook图片OSS端点

#### COOK_IMG_OSS_BUCKET

Cook图片OSS桶

#### COOK_USE_API_ENV

Cook API 环境，默认值为`prod`

#### API_URL_TEST

测试API地址，默认值为`http://ai-shifu-api:5800/api`

#### API_URL_PROD

生产API地址，默认值为`http://ai-shifu-api-prod:5800/api`

#### COOK_LOG_LEVEL

Cook日志级别，默认值为`DEBUG`

#### COOK_LOG_OUT_LEVEL

Cook输出日志级别，默认值为`DEBUG`

#### COOK_LOG_DIR

Cook日志目录，默认值为`/var/log/`

#### COOK_LOG_OUT_PATH

Cook输出日志路径，默认值为`/var/log/cook.log`

#### COOK_LOG_ERR_LEVEL

Cook错误日志级别，默认值为`ERROR`

#### COOK_LOG_ERR_PATH

Cook错误日志路径，默认值为`/var/log/cook.err.log`
