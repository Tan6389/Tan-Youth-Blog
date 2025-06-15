---
title: 在中国使用giffgaff电话卡
cover: https://cdn-fusion.imgcdn.store/i/2025/XaDGJVksdz3Eh68u.jpg
swiper_index: 10
top_group_index: 10
background: '#fff'
date: 2025-06-14 10:33:30
updated:
tags: 通讯
categories: 通讯
keywords:
description:
top:
top_img:
comments:
toc:
toc_number:
toc_style_simple:
copyright:
copyright_author:
copyright_author_href:
copyright_url:
copyright_info:
mathjax:
katex:
aplayer:
highlight_shrink:
aside:
ai:
---
# 🇬🇧 如何在中国大陆使用 giffgaff SIM（从购买到彻底关闭语音信箱）

很多人为了备用手机号、收取认证码或者测试项目，会购买一张 **giffgaff SIM卡**（英国虚拟运营商，按需充值，无月租），但是 giffgaff 本身主要为 **英国境内设计**，我们身在中国时需要做一些设置和准备。

本文将手把手地说清楚以下环节：

✅ 如何购买 giffgaff SIM
✅ 如何激活 SIM
✅ 如何插卡设置
✅ 如何彻底**免费地**关闭语音信箱（以免产生附加收费）
✅ 小贴士：建议准备的操作（数据设置、API 检查）

---

## 🔹购买 giffgaff SIM卡

建议可以通过以下几种方式购买：

- **官网申请**：可以在 giffgaff [官网](https://www.giffgaff.com/) 免费申请 SIM，邮寄到你的转运公司。
- **淘宝/闲鱼**：可以购买别人转让出的 giffgaff SIM，通常几元就可以到手。

---

## 🔹准备工作

收到 SIM卡后，你需要准备以下几样东西：

✅ 一部解锁且支持 GSM 的智能手机号（建议备用机）
✅ 一张 giffgaff SIM卡
✅ 一根取卡针

---

## 🔹激活 giffgaff SIM卡（建议有 VPN时进行）

1️⃣ 打开 giffgaff 官网 [https://www.giffgaff.com/activate](https://www.giffgaff.com/activate)  
2️⃣ 输入你的 SIM 卡背后印有的 6 位激活码  
3️⃣ 绑定你的电子邮件进行账号设置  
4️⃣ 依提示为 SIM 充值最少 £10，建议可以购买一个最便宜的 **goodybag**（套餐），以便激活时可以进行数据/语音测试。

---

## 🔹插卡设置

✅ 关机  
✅ 插入 giffgaff SIM到备用机中（建议放在 SIM 2 槽）  
✅ 开机，若设置为中文，建议可以在设置中修改为英文，方便调试  

---

## 🔹彻底免费地关闭语音信箱（推荐）

我们可以通过 **GSM代码**彻底解除语音信箱转接设置，完全免费，且适用全球。

1️⃣ 打开“拨号”应用  
2️⃣ 依次输入以下代码：
```shell
##004#
````

3️⃣ 轻触“拨号”按键
4️⃣ 几秒后，你将收到“所有转移均已解除”的提示

---

## 🔹验证语音信箱已彻底停用

可以用你的 **另一部手机号**拨打 giffgaff 这张 SIM：

* 让它一直响到无人接听
* 这时**电话将自动挂断**而不是转到语音信箱，表明设置成功。

---

## 🔹建议设置（数据设置）

🚀 为防止 **数据流量自动消耗**，建议可以：

* 进入设置 > SIM设置
* 手动**禁用 giffgaff 的移动数据**
  这样，即使插卡时数据开关不小心打开，你也不会产生数据收费。

---

## 🔹API 小贴士（适用有 ADB 的用户）

如你可以通过 ADB 控制你的备用机，你可以这样：

```shell
adb shell settings put global mobile_data 0
```

这句话可以彻底**关掉数据**，以防止 SIM 自动消耗数据。

---

## 🔹结论

这样，你就可以：
✅ 在中国大陆纯备用地使用 giffgaff SIM
✅ 能轻松收取 SMS（包括认证码）
✅ 不必担心语音信箱和数据消耗产生附加收费

---
