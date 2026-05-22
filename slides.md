---
theme: seriph
background: https://picsum.photos/id/1043/1280/720
class: text-center flex flex-col items-center justify-center h-full
highlighter: shiki
lineNumbers: false
info: |
  ## 小红书自动化工具 MCP Server 项目介绍
title: 小红书 AI 评论自动化工具 · 基于 Playwright + MCP 架构
---

# 小红书 AI 自动化工具
## Playwright + MCP 智能搜索评论系统

<div class="mt-10 px-8">
  <div class="bg-white/20 backdrop-blur-md rounded-full px-6 py-3 inline-block text-white/90 text-lg mb-3">
    基于 MCP 协议 · AI 智能评论 · 自动化运营
  </div>
</div>

<div class="mt-6 text-white/80 text-lg">
  汇报人：胡欣然 &nbsp;&nbsp;|&nbsp;&nbsp; 2026年5月
</div>
---
background: #fafafa
class: flex flex-col justify-center items-center
---

# 目录
## CONTENTS

<div class="grid grid-cols-2 gap-8 mt-8 w-full max-w-4xl">
  <div>
    <p class="text-2xl font-bold text-pink-500">01</p>
    <h3 class="text-xl font-semibold">项目介绍</h3>
    <p class="text-gray-500 text-sm">工具定位 · 核心优势</p>
  </div>
  <div>
    <p class="text-2xl font-bold text-pink-500">02</p>
    <h3 class="text-xl font-semibold">核心功能</h3>
    <p class="text-gray-500 text-sm">登录 · 搜索 · 获取 · 评论</p>
  </div>
  <div>
    <p class="text-2xl font-bold text-pink-500">03</p>
    <h3 class="text-xl font-semibold">安装步骤</h3>
    <p class="text-gray-500 text-sm">环境 · 依赖 · 浏览器</p>
  </div>
  <div>
    <p class="text-2xl font-bold text-pink-500">04</p>
    <h3 class="text-xl font-semibold">MCP 配置</h3>
    <p class="text-gray-500 text-sm">Mac / Windows 配置</p>
  </div>
  <div>
    <p class="text-2xl font-bold text-pink-500">05</p>
    <h3 class="text-xl font-semibold">使用方法</h3>
    <p class="text-gray-500 text-sm">指令 · 流程 · 示例</p>
  </div>
  <div>
    <p class="text-2xl font-bold text-pink-500">06</p>
    <h3 class="text-xl font-semibold">问题与声明</h3>
    <p class="text-gray-500 text-sm">常见报错 · 免责说明</p>
  </div>
</div>

---
layout: default
background: #fdfbfb
color: #222
class: px-8 py-6
---

# 01 项目介绍
## 小红书 MCP 自动化评论工具

<div class="mt-6 bg-white rounded-xl shadow p-6">
  <div class="mb-6">
    <h3 class="text-pink-500 font-bold text-lg">🎯 项目定位</h3>
    <p class="mt-1 text-gray-700 text-base">
基于Playwright开发小红书自动化工具，作为MCP Server提供标准接口，可对接Claude等MCP客户端，完成小红书全流程自动化操作。
    </p>
  </div>

  <div class="mb-6">
    <h3 class="text-pink-500 font-bold text-lg">⚡ 核心价值</h3>
    <ul class="mt-1 text-gray-700 text-base list-disc pl-5 space-y-1">
      <li>持久化登录，一次扫码长期免登</li>
      <li>关键词搜索，批量获取小红书笔记</li>
      <li>智能解析笔记，提取标题、作者与正文</li>
      <li>AI生成评论，自动发布提升运营效率</li>
    </ul>
  </div>

  <div class="grid grid-cols-2 gap-6">
    <div>
      <h3 class="text-pink-500 font-bold text-lg">🧩 技术架构</h3>
      <p class="mt-1 text-gray-700 text-base">
AI客户端 → MCP协议 → Playwright自动化 → 小红书平台
      </p>
    </div>
    <div>
      <h3 class="text-pink-500 font-bold text-lg">✨ 适用场景</h3>
      <p class="mt-1 text-gray-700 text-base">
内容运营、笔记互动、账号养号、竞品采集、智能种草、自动化引流
      </p>
    </div>
  </div>
</div>
---
layout: two-cols
background: #FFF0F6
class: px-8 py-6
---

# 工具定位与介绍
## 小红书 MCP 自动化工具核心解析

::left::
### 📌 工具定位
<div class="bg-white rounded-xl shadow-sm p-5 border border-pink-100 mt-4">
  <p class="text-gray-700 leading-relaxed">
    基于 <strong class="text-pink-500">Playwright</strong> 开发的专业小红书自动化运营工具，部署为标准 <strong class="text-pink-500">MCP Server</strong>，可无缝接入 Claude、ChatGPT 等任意 MCP 客户端，无需复杂开发，即可实现小红书全流程自动化操作，大幅提升运营效率。
  </p>
</div>

### 🔄 运行架构
<div class="bg-white rounded-xl shadow-sm p-5 border border-pink-100 mt-6">
  <p class="text-gray-700 font-medium mb-2">完整架构链路：</p>
  <div class="flex items-center justify-around text-center text-gray-600">
    <span class="font-semibold">MCP Client<br/>(AI客户端)</span>
    <span class="text-pink-500 text-2xl">↔</span>
    <span class="font-semibold">MCP Server<br/>(本工具)</span>
    <span class="text-pink-500 text-2xl">↔</span>
    <span class="font-semibold">小红书<br/>(浏览器自动化)</span>
  </div>
  <p class="text-xs text-gray-500 mt-3 text-center">通过 MCP 协议通信，实现指令下发与结果返回，全程自动化无人工干预</p>
</div>

::right::
<div class="flex flex-col items-center justify-center h-full bg-white rounded-xl shadow-sm p-6 border border-pink-100">
  <img src="https://picsum.photos/id/180/400/300" class="rounded-xl shadow-md border border-gray-200" />
  <p class="text-gray-600 mt-4 font-medium">MCP 自动化架构示意图</p>
  <p class="text-xs text-gray-500 mt-2 text-center">
    左侧 AI 客户端负责指令发起与评论生成，中间本工具作为服务端执行自动化操作，右侧对接小红书平台完成交互
  </p>
  <div class="mt-4 w-full h-1 bg-pink-100 rounded-full"></div>
  <p class="text-pink-500 text-sm mt-4 font-semibold">核心优势：低代码、高兼容、易操作</p>
</div>

---
background: #fff
class: px-10 py-8
---

# 主要特点与优势
## 四大核心优势，赋能自动化运营
<div class="grid grid-cols-2 gap-6 mt-6">
  <div class="p-6 rounded-2xl bg-pink-50 border border-pink-100 shadow-sm hover:shadow-md transition-shadow duration-300">
    <div class="flex items-center gap-3 mb-2">
      <span class="text-pink-500 text-xl">✅</span>
      <h4 class="font-bold text-lg text-pink-700">深度集成 AI 能力</h4>
    </div>
    <p class="text-sm text-gray-600 leading-relaxed">
      无缝对接 MCP 客户端大模型，生成贴合笔记内容、语气自然、相关性强的评论，避免机械感，提升互动质量。
    </p>
  </div>

  <div class="p-6 rounded-2xl bg-blue-50 border border-blue-100 shadow-sm hover:shadow-md transition-shadow duration-300">
    <div class="flex items-center gap-3 mb-2">
      <span class="text-blue-500 text-xl">✅</span>
      <h4 class="font-bold text-lg text-blue-700">模块化设计</h4>
    </div>
    <p class="text-sm text-gray-600 leading-relaxed">
      拆分笔记分析、评论生成、评论发布三大独立模块，降低维护成本，可根据需求灵活调整单个模块功能。
    </p>
  </div>

  <div class="p-6 rounded-2xl bg-purple-50 border border-purple-100 shadow-sm hover:shadow-md transition-shadow duration-300">
    <div class="flex items-center gap-3 mb-2">
      <span class="text-purple-500 text-xl">✅</span>
      <h4 class="font-bold text-lg text-purple-700">强大内容获取</h4>
    </div>
    <p class="text-sm text-gray-600 leading-relaxed">
      集成4种差异化内容获取方案，适配不同类型笔记，有效规避页面渲染问题，确保完整抓取笔记标题、作者、正文等核心信息。
    </p>
  </div>

  <div class="p-6 rounded-2xl bg-green-50 border border-green-100 shadow-sm hover:shadow-md transition-shadow duration-300">
    <div class="flex items-center gap-3 mb-2">
      <span class="text-green-500 text-xl">✅</span>
      <h4 class="font-bold text-lg text-green-700">持久化登录 + 两步式评论</h4>
    </div>
    <p class="text-sm text-gray-600 leading-relaxed">
      首次扫码登录后保存会话状态，后续无需重复操作；采用“先分析笔记→再生成评论→最后发布”的两步流程，提升操作稳定性。
    </p>
  </div>
</div>

---
background: #fff
class: px-10 py-8
---

# 2.0 版本核心优化
## 迭代升级 · 体验与性能双提升
<div class="mt-2 text-gray-500 text-base">基于1.0版本优化迭代，聚焦稳定性、实用性，适配更多场景需求</div>

<div class="grid grid-cols-1 md:grid-cols-2 gap-5 mt-6">
  <div class="p-5 rounded-xl bg-pink-50 border border-pink-100 shadow-sm">
    <div class="flex items-center gap-3 mb-2">
      <span class="text-pink-500 font-bold text-xl">✅</span>
      <h4 class="font-bold text-pink-700">内容获取增强</h4>
    </div>
    <p class="text-sm text-gray-600">重构内容获取核心模块，新增页面等待、滚动加载机制，集成4种差异化获取方案，彻底解决笔记内容抓取不完整、加载失败等问题。</p>
  </div>

  <div class="p-5 rounded-xl bg-blue-50 border border-blue-100 shadow-sm">
    <div class="flex items-center gap-3 mb-2">
      <span class="text-blue-500 font-bold text-xl">✅</span>
      <h4 class="font-bold text-blue-700">AI 评论生成优化</h4>
    </div>
    <p class="text-sm text-gray-600">将评论生成逻辑移交至 MCP 客户端，依托大模型能力，生成更贴合笔记主题、语气自然、无机械感的评论，提升互动真实性。</p>
  </div>

  <div class="p-5 rounded-xl bg-purple-50 border border-purple-100 shadow-sm">
    <div class="flex items-center gap-3 mb-2">
      <span class="text-purple-500 font-bold text-xl">✅</span>
      <h4 class="font-bold text-purple-700">功能模块化重构</h4>
    </div>
    <p class="text-sm text-gray-600">拆分笔记分析、评论生成、评论发布三大独立模块，降低代码耦合度，便于后续功能迭代、bug修复，提升整体可维护性。</p>
  </div>

  <div class="p-5 rounded-xl bg-green-50 border border-green-100 shadow-sm">
    <div class="flex items-center gap-3 mb-2">
      <span class="text-green-500 font-bold text-xl">✅</span>
      <h4 class="font-bold text-green-700">搜索结果与错误处理优化</h4>
    </div>
    <p class="text-sm text-gray-600">修复搜索结果标题不显示的核心bug；新增详细日志打印与调试信息输出，快速定位问题、排查异常，提升工具稳定性。</p>
  </div>
</div>

<!-- 优化图片样式，贴合整体风格，增加说明 -->
<div class="flex justify-center mt-8">
  <div class="bg-white p-3 rounded-xl shadow-md border border-gray-100">
    <img src="https://picsum.photos/id/3/600/280" class="rounded-lg" />
    <p class="text-center text-sm text-gray-500 mt-3">版本迭代优化示意图 · 功能更稳定、操作更流畅</p>
  </div>
</div>
---
layout: cover
background: https://picsum.photos/id/1041/1280/720
class: text-white flex flex-col items-center justify-center text-center p-8
---

# 02 核心功能
## 全流程自动化 · 赋能高效运营
### 覆盖小红书运营核心场景，实现从登录到评论的全自动化闭环

<div class="absolute inset-0 bg-black/40 backdrop-blur-sm"></div>
<div class="relative z-10 flex flex-col items-center justify-center h-full">
  <!-- 主标题区域 -->
  <div class="mb-10">
    <h1 class="text-6xl font-bold tracking-wider mb-4">02 核心功能</h1>
    <h2 class="text-3xl text-white/90 mb-2">全流程自动化 · 赋能高效运营</h2>
    <p class="text-white/70 text-lg">覆盖小红书运营核心场景，实现从登录到评论的全自动化闭环</p>
  </div>

  <!-- 核心功能亮点卡片 -->
  <div class="grid grid-cols-2 md:grid-cols-4 gap-4 w-full max-w-5xl">
    <div class="bg-white/10 backdrop-blur-md rounded-xl p-4 hover:bg-white/20 transition-all duration-300">
      <p class="text-xl font-bold mb-2">🔐 持久化登录</p>
      <p class="text-sm text-white/80">一次扫码，长期免登，自动保存会话</p>
    </div>
    <div class="bg-white/10 backdrop-blur-md rounded-xl p-4 hover:bg-white/20 transition-all duration-300">
      <p class="text-xl font-bold mb-2">🔍 智能搜索</p>
      <p class="text-sm text-white/80">关键词搜索，批量获取目标笔记</p>
    </div>
    <div class="bg-white/10 backdrop-blur-md rounded-xl p-4 hover:bg-white/20 transition-all duration-300">
      <p class="text-xl font-bold mb-2">📝 内容解析</p>
      <p class="text-sm text-white/80">精准提取笔记标题、作者、正文信息</p>
    </div>
    <div class="bg-white/10 backdrop-blur-md rounded-xl p-4 hover:bg-white/20 transition-all duration-300">
      <p class="text-xl font-bold mb-2">🤖 AI 评论</p>
      <p class="text-sm text-white/80">智能生成评论，全自动发布互动</p>
    </div>
  </div>

  <!-- 底部点缀 -->
  <div class="mt-10 border-t border-white/20 w-1/3 pt-3">
    <p class="text-white/60 text-sm">Playwright + MCP 双架构 · 稳定高效 · 易操作</p>
  </div>
</div>
---
background: #fff
class: px-6 py-4
---

# 核心功能详解（一）
## 用户认证与内容获取
<p class="text-sm text-gray-500 mt-1">从登录安全到内容抓取，全流程稳定高效</p>

### 一、用户认证与登录
<div class="grid grid-cols-2 gap-4 mt-3">
  <div class="p-4 rounded-xl bg-pink-50 border border-pink-100 shadow-sm">
    <div class="flex items-center gap-2 mb-2">
      <span class="text-pink-500 text-lg">🔐</span>
      <h3 class="text-base font-bold text-pink-700">持久化登录</h3>
    </div>
    <ul class="space-y-1 text-xs text-gray-600 pl-1">
      <li class="flex items-start gap-1">
        <span class="text-pink-500 mt-0.5">✅</span>
        <span>首次手动扫码登录，符合平台规范</span>
      </li>
      <li class="flex items-start gap-1">
        <span class="text-pink-500 mt-0.5">✅</span>
        <span>自动保存登录状态，加密存储会话</span>
      </li>
      <li class="flex items-start gap-1">
        <span class="text-pink-500 mt-0.5">✅</span>
        <span>后续免重复登录，使用更高效</span>
      </li>
    </ul>
  </div>

  <div class="p-4 rounded-xl bg-blue-50 border border-blue-100 shadow-sm">
    <div class="flex items-center gap-2 mb-2">
      <span class="text-blue-500 text-lg">📊</span>
      <h3 class="text-base font-bold text-blue-700">状态管理</h3>
    </div>
    <ul class="space-y-1 text-xs text-gray-600 pl-1">
      <li class="flex items-start gap-1">
        <span class="text-blue-500 mt-0.5">✅</span>
        <span>启动自动检测当前登录状态</span>
      </li>
      <li class="flex items-start gap-1">
        <span class="text-blue-500 mt-0.5">✅</span>
        <span>失效自动提醒，引导重新登录</span>
      </li>
      <li class="flex items-start gap-1">
        <span class="text-blue-500 mt-0.5">✅</span>
        <span>安全校验，保障账号稳定安全</span>
      </li>
    </ul>
  </div>
</div>

### 二、内容发现与获取
<div class="mt-4 p-4 rounded-xl bg-purple-50 border border-purple-100 shadow-sm">
  <div class="flex items-center gap-2 mb-2">
    <span class="text-purple-500 text-lg">🔍</span>
    <h3 class="text-base font-bold text-purple-700">多维度内容抓取</h3>
  </div>
  <ul class="space-y-1 text-xs text-gray-600 pl-1">
    <li class="flex items-start gap-1">
      <span class="text-purple-500 mt-0.5">✅</span>
      <span><strong>关键词搜索</strong>：自定义关键词，可指定获取数量</span>
    </li>
    <li class="flex items-start gap-1">
      <span class="text-purple-500 mt-0.5">✅</span>
      <span><strong>4种获取方案</strong>：适配不同笔记，确保信息完整</span>
    </li>
    <li class="flex items-start gap-1">
      <span class="text-purple-500 mt-0.5">✅</span>
      <span><strong>评论区抓取</strong>：获取评论人、内容、发布时间</span>
    </li>
  </ul>
</div>
---
background: #fff
class: px-8 py-5
---

# 三、内容分析与生成
## 智能解析 + AI 创作 · 提升互动质量
<div class="text-sm text-gray-500 mt-1 mb-4">自动分析笔记内容，AI生成多风格评论，满足不同运营需求</div>

<div class="grid grid-cols-2 gap-5 mt-4">
  <div class="p-5 rounded-2xl bg-pink-50 border border-pink-100 shadow-sm">
    <div class="flex items-center gap-2 mb-3">
      <span class="text-pink-500 text-xl">📝</span>
      <h3 class="text-lg font-bold text-pink-700">笔记智能分析</h3>
    </div>
    <ul class="space-y-2 text-sm text-gray-600">
      <li class="flex items-center gap-2">
        <span class="text-pink-500">✅</span>
        <span>精准提取标题、作者、正文内容</span>
      </li>
      <li class="flex items-center gap-2">
        <span class="text-pink-500">✅</span>
        <span>自动识别领域与核心关键词</span>
      </li>
      <li class="flex items-center gap-2">
        <span class="text-pink-500">✅</span>
        <span>返回结构化 JSON 数据，便于使用</span>
      </li>
    </ul>
  </div>

  <div class="p-5 rounded-2xl bg-orange-50 border border-orange-100 shadow-sm">
    <div class="flex items-center gap-2 mb-3">
      <span class="text-orange-500 text-xl">🤖</span>
      <h3 class="text-lg font-bold text-orange-700">AI 多风格评论</h3>
    </div>
    <ul class="space-y-2 text-sm text-gray-600">
      <li class="flex items-center gap-2">
        <span class="text-orange-500">✅</span>
        <span>引流型 → 引导关注/私聊，提升粉丝</span>
      </li>
      <li class="flex items-center gap-2">
        <span class="text-orange-500">✅</span>
        <span>互动型 → 友好赞美，快速提升好感</span>
      </li>
      <li class="flex items-center gap-2">
        <span class="text-orange-500">✅</span>
        <span>咨询型 → 主动提问，有效增加互动率</span>
      </li>
      <li class="flex items-center gap-2">
        <span class="text-orange-500">✅</span>
        <span>专业型 → 输出知识，树立专业形象</span>
      </li>
    </ul>
  </div>
</div>

---
layout: cover
background: https://picsum.photos/seed/mcp3/1280/720
class: text-white flex flex-col items-center justify-center h-full
---

<!-- 半透明深色遮罩 -->
<div class="absolute inset-0 bg-black/45 backdrop-blur-sm"></div>

<!-- 居中内容 -->
<div class="relative z-10 text-center px-6">
  <h1 class="text-6xl font-bold tracking-wider mb-6">
    03 安装步骤
  </h1>
  <h2 class="text-3xl font-medium text-white/90 mb-4">
    环境搭建全流程
  </h2>
  <p class="text-lg text-white/70 mt-2 max-w-xl mx-auto">
    从Python环境 → 项目部署 → 依赖安装 → 浏览器内核配置
    <br>一站式完整搭建教程
  </p>

  <!-- 简约分隔线 -->
  <div class="w-40 h-1 bg-white/30 rounded-full mx-auto mt-8"></div>

  <!-- 底部小字 -->
  <p class="text-white/60 text-sm mt-6">
    Playwright + MCP 项目 · 标准化部署流程
  </p>
</div>
---
background: #fff
class: px-8 py-6
---

# 03 安装步骤
## ① 安装 Python 环境
<div class="text-sm text-gray-500 mt-1 mb-6">确保系统已安装 Python 3.8 或更高版本，这是运行本工具的基础环境</div>

<div class="grid grid-cols-1 md:grid-cols-2 gap-6">
  <div class="p-6 rounded-2xl bg-pink-50 border border-pink-100 shadow-sm">
    <div class="flex items-center gap-3 mb-4">
      <span class="text-pink-500 text-2xl">🐍</span>
      <h3 class="text-lg font-bold text-pink-700">版本要求</h3>
    </div>
    <ul class="space-y-2 text-sm text-gray-600">
      <li class="flex items-center gap-2">
        <span class="text-pink-500">✅</span>
        <span><strong>推荐版本：</strong>Python 3.8 ~ 3.12</span>
      </li>
      <li class="flex items-center gap-2">
        <span class="text-pink-500">✅</span>
        <span><strong>官网下载：</strong><a href="https://www.python.org/downloads/" class="text-blue-500 hover:underline">python.org/downloads</a></span>
      </li>
      <li class="flex items-center gap-2">
        <span class="text-pink-500">⚠️</span>
        <span><strong>安装必选：</strong>勾选 "Add Python to PATH"</span>
      </li>
    </ul>
  </div>

  <div class="p-6 rounded-2xl bg-white border border-gray-200 shadow-sm">
    <img src="https://picsum.photos/id/0/500/300" class="w-full h-40 object-cover rounded-lg" />
    <p class="text-center text-sm text-gray-500 mt-3">Python 安装界面示例</p>
  </div>
</div>
---
background: #fff
class: px-6 py-5
---

# 03 安装步骤
## ② 获取项目源码

<div class="mt-3 mb-5 text-sm text-gray-500">
  将项目文件下载到本地，准备后续环境配置
</div>

<div class="bg-blue-50 rounded-xl p-5 border border-blue-100 shadow-sm mb-5">
  <div class="flex items-center gap-2 mb-4">
    <span class="text-blue-500 text-xl">📦</span>
    <h3 class="font-bold text-blue-700">操作步骤</h3>
  </div>
  <ol class="text-gray-700 space-y-3 pl-6 list-decimal">
    <li>下载项目压缩包并完成解压</li>
    <li class="font-medium text-blue-700">【重要】文件路径不能包含中文与空格</li>
    <li>打开终端工具，进入项目所在根目录</li>
  </ol>
</div>

<div class="bg-white rounded-xl p-4 border border-gray-200 shadow-sm">
  <div class="w-full h-40 bg-gray-100 rounded-lg flex items-center justify-center text-gray-400">
    项目目录结构示意图
  </div>
  <p class="text-center text-sm text-gray-500 mt-3">
    项目文件目录结构示例
  </p>
</div>
---
background: #fff
class: px-6 py-5
---

# 03 安装步骤
## ③ 创建并激活虚拟环境

<div class="mt-2 text-sm text-gray-500 mb-5">
  使用虚拟环境隔离依赖，防止版本冲突，保证项目稳定运行
</div>

<div class="bg-purple-50 rounded-xl p-5 border border-purple-100 shadow-sm">
  <div class="flex items-center gap-2 mb-4">
    <span class="text-purple-500 text-xl">🔧</span>
    <h3 class="font-bold text-purple-700">操作指令</h3>
  </div>

  <div class="bg-white rounded-lg p-3 mb-3">
    <p class="text-xs font-semibold text-gray-700 mb-1">1. 创建虚拟环境</p>
    <div class="bg-gray-100 px-3 py-2 rounded text-sm font-mono">
      python3 -m venv venv
    </div>
  </div>

  <div class="bg-white rounded-lg p-3">
    <p class="text-xs font-semibold text-gray-700 mb-1">2. 激活虚拟环境</p>
    <div class="bg-gray-100 px-3 py-2 rounded text-sm font-mono mb-1">
      # Windows
      venv\Scripts\activate
    </div>
    <div class="bg-gray-100 px-3 py-2 rounded text-sm font-mono">
      # Mac/Linux
      source venv/bin/activate
    </div>
  </div>
</div>

<div class="mt-4 text-purple-500 text-sm font-medium text-center">
  激活成功后，终端前方会显示 (venv) 标识
</div>
---
background: #fff
class: px-6 py-5
---

# 03 安装步骤
## ④ 安装项目依赖

<div class="mt-2 text-sm text-gray-500 mb-5">
  安装项目所需Python库，包含 Playwright、fastmcp 等核心依赖
</div>

<div class="bg-green-50 rounded-xl p-5 border border-green-100 shadow-sm">
  <div class="flex items-center gap-2 mb-4">
    <span class="text-green-500 text-xl">📦</span>
    <h3 class="font-bold text-green-700">核心安装命令</h3>
  </div>

  <div class="bg-white rounded-lg p-3 mb-3">
    <p class="text-xs font-semibold text-gray-700 mb-1">1. 安装基础依赖</p>
    <div class="bg-gray-100 px-3 py-2 rounded text-sm font-mono">
      pip install -r requirements.txt
    </div>
  </div>

  <div class="bg-white rounded-lg p-3">
    <p class="text-xs font-semibold text-gray-700 mb-1">2. 安装 MCP 服务框架</p>
    <div class="bg-gray-100 px-3 py-2 rounded text-sm font-mono">
      pip install fastmcp
    </div>
  </div>
</div>

<div class="mt-4 text-center text-green-600 font-medium text-sm">
  等待安装完成，无报错即成功
</div>

---
background: #fff
class: px-6 py-5
---

# 03 安装步骤
## ⑤ 安装 Playwright 浏览器

<div class="mt-2 text-sm text-gray-500 mb-5">
  安装 Playwright 自动化所需的浏览器内核（Chromium、Firefox、WebKit）
</div>

<div class="bg-orange-50 rounded-xl p-5 border border-orange-100 shadow-sm">
  <div class="flex items-center gap-2 mb-4">
    <span class="text-orange-500 text-xl">🌐</span>
    <h3 class="font-bold text-orange-700">浏览器安装命令</h3>
  </div>

  <div class="bg-white rounded-lg p-3 mb-3">
    <p class="text-xs font-semibold text-gray-700 mb-1">执行安装命令</p>
    <div class="bg-gray-100 px-3 py-2 rounded text-sm font-mono">
      playwright install
    </div>
  </div>

  <div class="text-sm text-gray-600">
    <p class="font-medium">安装说明：</p>
    <p>此命令会自动下载并安装Chromium、Firefox、WebKit等浏览器内核，用于自动化操作。</p>
  </div>
</div>

<div class="mt-4 text-center text-orange-600 font-medium text-sm">
  等待安装完成，无报错即成功
</div>
---
layout: cover
background: https://picsum.photos/id/1043/1280/720
class: text-white flex items-center justify-center h-full
---

<div class="absolute inset-0 bg-black/40 backdrop-blur-md"></div>

<div class="relative z-10 text-center px-6">
  <h1 class="text-6xl font-bold mb-8">感谢观看</h1>
  
  <div class="bg-white/20 backdrop-blur-md rounded-full px-8 py-4 inline-block mb-8">
    <p class="text-2xl font-semibold">Q & A</p>
    <p class="text-white/80 text-lg mt-2">欢迎提问交流</p>
  </div>

  <div class="text-white/70 text-sm">
    <p>汇报人：胡欣然</p>
    <p>2026 年 5 月</p>
  </div>
</div>
