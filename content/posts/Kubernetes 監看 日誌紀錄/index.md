---
title: "Kubernetes 監看 日誌紀錄"
subtitle: ""
date: 2021-02-24T22:31:49+08:00
lastmod: 2021-02-24T22:31:49+08:00
draft: false
author: ""
description: ""
resources:
- name: "featured-image"
  src: "featured-image.png"

page:
    theme: "wide"

upd: ""
authorComment: ""

tags: ["Kubernetes", "k8s", "Monitoring"]
categories: ["DevOps"]

hiddenFromHomePage: false
hiddenFromSearch: false

featuredImage: ""
featuredImagePreview: ""

toc:
  enable: true
math:
  enable: false
lightgallery: true
comments: true
license: license = '<a rel="license external nofollow noopener noreffer" href="https://creativecommons.org/licenses/by-nc/4.0/" target="_blank">CC BY-NC 4.0</a>'
---
# Kubernetes 監看 日誌紀錄

## 指標與日誌

* 指標 (Metrics)
> 在一段時間測量而得的一連串數字

* 日誌 (Logs)
> 用來對系統進行探索分析

## 監看的技術

* 黑箱監看
> 從應用程式外部進行監看, 監看 CPU, 記憶體, 儲存設備
> 但他缺乏對應用程式如何運作的背景知識

* 白箱監看
> 專注在應用程式狀態的背景詳情, 如 HTTP 請求數, 500號錯誤訊息總數 (500代表伺服器內部錯誤(internal server)), 請求延遲時間

## 監看模式




