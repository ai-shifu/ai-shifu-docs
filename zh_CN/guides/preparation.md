# 部署前的准备工作

目前 AI师傅（AI-Shifu）自有的剧本编辑调试工具还在设计阶段，作为创业团队，在时间和资源有限的情况下，我们选择践行敏捷和精益的思想 -- 使用飞书的多维表格作为我们的剧本载体

因此，我们的准备工作有以下两部分：
* [**飞书应用准备及配置**](#飞书应用的准备及配置)
* [**AI师傅剧本（即飞书多维表格）的准备及配置**](#AI师傅剧本的准备及配置)


## 飞书应用的准备及配置

我们需要在 `飞书开放平台` 中创建一个飞书应用，以便在系统中能够对相应的剧本文档进行操作

### Step01: 登录飞书开放平台

☞ https://open.feishu.cn
<img src="../../img/zh-login-feishu-open.png" alt="">

### Step02: 创建 `企业自建应用`

<img src="../../img/zh-feishu-create-app.png" alt="">

### Step03: 填写应用必要信息

* 应用名称： AI师傅
* 应用描述： 用于AI师傅操作飞书多维表格

<img src="../../img/zh-feishu-create-app-enter-info.png" alt="">

### Step04: 添加应用能力

创建完应用后，默认会跳转到 `添加应用能力` 页面，如若没有跳转，可以点击左侧导航 `应用能力` 下面的 `添加应用能力`

我们只需添加 `机器人` 这一项能力即可

<img src="../../img/zh-feishu-create-app-add-ability.png" alt="">

点击添加后，`应用能力` 下面的出现了 `机器人` 这一项能力即代表添加成功。此时我们不需要做任何其他配置。

<img src="../../img/zh-feishu-create-app-add-ability-done.png" alt="">

### Step05: 添加必要权限

* 点击左侧导航中的 `权限管理`
* 在搜索框中搜索 `bit`
* 找到权限 `查看、评论、编辑和管理多维表格`
* 点击右侧的 `开通权限`
* 由于我们开通的是免审权限，此时权限状态应该是 $${\color{green}•已开通}$$

<img src="../../img/zh-feishu-create-app-auth.png" alt="">

### Step06: 发布应用

要使当前应用及其配置生效还需要创建版本并发布才可以。
* 点击顶部提示中的 `创建版本`
* 填写必要信息
  * 版本号： 1.0.0
  * 更新说明： init ai-shifu
  * xx端默认能力： 默认勾选了 `机器人` 不用动

<img src="../../img/zh-feishu-create-app-create-version.png" alt="">

点击底部的 `保存` 按钮

<img src="../../img/zh-feishu-create-app-create-version-save.png" alt="">

如果你是管理员，那会立刻跳转到发布页面并弹出确认发布对话框，此时点击确认发布即可。 如果你不是管理员，则通知管理员审核发布。

<img src="../../img/zh-feishu-create-app-create-version-publish.png" alt="">

### Step07: 妥善保存应用凭证

🎉恭喜你已经完成飞书应用的准备工作了，请妥善保管好该应用的 ID 和 Secret

后续部署系统时，需要将其填写到 docker/.env 文件中的 `LARK_APP_ID` 和 `LARK_APP_SECRET` 变量中


----


## AI师傅剧本的准备及配置

123
