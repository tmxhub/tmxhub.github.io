---
categories: [大模型, API]
date: 2025-05-17 22:10:00 +0800
last_modified_at: 2025-05-17 22:30:00 +0800
tags: [LLM, API]
title: 如何获取公网免费大模型API？
pin: false
toc: true
comments: true
image:
  path: /img/free-llm-api-on-the-public-network.jpg
---
大模型的优势和帮助想必大家已经有目共睹了，很多学生党可能也想使用大模型，但很多平台提供的大模型api有额度，亦或者不想受限于某平台或某软件，不满足于简单的问答需求，而是想通过api来做进一步的开发等。那什么办法免费薅到免费的大模型api呢？

## 一、公网免费大模型api网站

![大模型api](/img/free-llm-api-on-the-public-network1.png){: .shadow}

可以访问 [https://fofa.info/](https://fofa.info/result?qbase64=cG9ydD0iMTE0MzQiICYmc3RhdHVzX2NvZGU9IjIwMCI%3D)

通过**port="11434" && status_code="200"**来搜索当前可以使用的api

![大模型api](/img/free-llm-api-on-the-public-network2.png){: .shadow}

点击URL旁边的链接图标，可以查看链接显示状态“Ollama is running”，如：http://47.101.67.217:11434/

![大模型api](/img/free-llm-api-on-the-public-network3.png){: .shadow}

将URL后缀加上**api/tags**，例如http://47.101.67.217:11434/改为http://47.101.67.217:11434/<span class="red-text">api/tags</span>后回车，可以查看运行的模型名称、参数大小等信息

![大模型api](/img/free-llm-api-on-the-public-network4.png){: .shadow}

将URL和模型信息填写到AI聊天客户端，如Chatbox、Cherry Studio，就可以免费调用大模型进行问答等。

{% include embed/video.html src='/video/free-llm-api-on-the-public-network.mp4' %}


