# 支持的大模型及配置

目前支持：
* OpenAI (e.g., gpt-4o, gpt-3.5-turbo)
* Zhipu (e.g., GLM-3, GLM-4)
* deepseek (e.g., deepseek-chat, deepseek-coder)
* Qianfan Platform (e.g., ERNIE-4.0-8K, ERNIE-Speed-8K)
* Bailian Platform (e.g., qwen-max, qwen2-72b-instruct)

> 注意：平台类的注册后需要开通所需模型才能使用，具体开通方式详见各自平台的官方文档

部署时需要将各自的 Key 配置到 .env 文件中，配置说明详见 [环境变量配置](https://github.com/ai-shifu/ai-shifu-doc/blob/main/zh_CN/guides/environment-variables.md#%E5%A4%A7%E6%A8%A1%E5%9E%8B%E7%9B%B8%E5%85%B3%E9%85%8D%E7%BD%AE)

欢迎 [贡献代码](https://github.com/ai-shifu/ai-shifu-doc/blob/main/zh_CN/guides/contributing.md) ，增加更多模型的支持
