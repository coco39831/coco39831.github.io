---
title: Linux新手入門指南
date: 2026-01-04 12:07:30
categories:
    - Linux
tags: Linux
---

## 怎麼麼有這麼多Linux？

嚴格來講，Linux只是單指Linux核心（Kernel），而平常看到的Arch Linux, Debian Linux以及其他的，這些全都是發行板，也就是其他人已經打包好的Linux。

---

## 拆解Linux發行版

通常一個發行版可分為幾個零件，核心（Kernel）、殼層（Shell）、圖形界面（Desktop Enviroment）。

### 核心（Kernel）

核心就如同它名字所說，它是整個作業系統的心臟，與硬體直接對話。
    功能： 資源分配、進程管理、硬體驅動
    比喻： 它就像是汽車引擎，你不會直接操作引擎來開車，但你又不能失去它。

### 殼層（Shell）

這是使用者與核心溝通的橋樑。當你在黑底白字的視窗輸入指令時，Shell會將這些指令翻譯給核心。
    常見種類： Bash（Bourne Again Shell）、Zsh
    比喻：汽車的腳踏板，你得通過這控制引擎。

---

## Limux 與 Windows 的核心差異

### 1.檔案系統：消失的C槽

| 系統 | 檔案結構邏輯 | 詳細說明 |
| :--- | :--- | :--- |
| **Windows** | 磁碟機代號 | 使用 `C:`、`D:\` 等代號區分不同分割區。 |
| **Linux** | 樹狀結構 (Tree Structure) | 一切都從根目錄 `/` (Root) 開始。<br>不同的硬碟分區只是「掛載（Mount）」在樹狀結構的某個資料夾下。<br>例如：`/home/user` 是你的家目錄，類似 Windows 的「使用者」資料夾。 |

### 2. 一切皆檔案

這是Unix/Linux的重要哲學。
    你的文件是檔案。
    你的硬碟也是檔案（/dev/sda）在系統看來也是檔案。
    你的鍵盤輸入、螢幕輸出在本質上也是資料流（stream）檔案。
    意義：你可以用同個指令處理文字檔、硬體設備、系統設定之類的。

### 3. 嚴格的權限管理

Linux是多使用者系統，每一個使用者都會有不的權限。
    Root（超級使用者）：擁有系統的生殺大權，可以刪除任何檔案（剛說過Linux系統下，一切皆文件，當然也包括系統本身）。
    一般使用者：只能修改自己的檔案。若要執行系統級別的操作，須暫時使用Root權限。

---

## 如何開始體驗Linux

你當然可以直接將你常用的電腦慣成Linux，但這並不推薦，因為完壞了要重來很麻煩，因此我推薦使用虛擬機來操作。
    1. WSL（Windows Subsystem for Linux）
        優點：直接在Windows上運行Linux，適合開發和學習指令。
        在Windows Powershell輸入wsl --install即可安裝Ubuntu。
    2. 虛擬機（Virtual Machine）:
        優點：擁有完整的界面，完壞了可以直接刪掉重來。
        工具：使用VirtualBox 或是 VMware
(這裡之後再出一篇文章細講)