# Information-security
## 目錄

* [Windows事件檢視器](#windows事件檢視器)

* [Windows排程管理員](#windows排程管理員)

* [Linux系統指令](#linux系統指令)

* [lucene 語法](#lucene-語法)

* [elasticsearch DSL 語法](#elasticsearch-dsl-語法)

## Windows事件檢視器

開始 → 執行 → 輸入 eventvwr 開啟事件檢視器

### Event Log
----------
|Event ID|Content|Event ID|Content|
|:------:|:------|:------:|:------|
|261|連線接收|4648|帳戶成功登入|
|1100|Windows已停止事件紀錄|4657|修改Registry value|
|1101|事件在傳輸過程被丟棄|4697|安裝新的服務|
|1102|事件紀錄檔已被清除|4688|已建立新的處理程序|
|1149|授權成功|4720|使用者帳戶已被成功創建|
|4104|執行Remote Command|4724|您嘗試重設帳戶密碼|
|4624|帳戶成功登入|7034|服務無預期關閉|
|4625|帳戶登入失敗|7036|服務啟動或是關閉|
|4634|帳戶已經登出|7040|服務啟動模式改變|
|4647|帳戶已經登出|

### Logon event type
---------------
|Type|Title|Description|
|:--:|:----|:----------|
|2|互動|使用者已登入這部電腦|
|3|網路|使用者或電腦從網路登入這部電腦|
|7|解除鎖定|輸入密碼登入使工作站解除鎖定|
|10|RemoteInteractive|使用者使用[終端機服務]或[遠端桌面]從遠端登入這部電腦|

### Logon/Logoff event difference
-------------------
Group A : Windows 2003 and before

Group B : Windows 2008 R2 and Windows 7 , Windows 2012 R2 and Windows 8.1 , Windows 2016 and Windows 10

|Group A event ID|Group B event ID|Content|
|:---:|:---:|:---|
|528|4624|帳戶成功登入|
|540|4624|帳戶成功登入|
|538|4634|帳戶已經登出|
|551|4647|帳戶已經登出|
|529|4625|帳戶登入失敗|
|530|4625|帳戶登入失敗|
|531|4625|帳戶登入失敗|
|532|4625|帳戶登入失敗|
|533|4625|帳戶登入失敗|
|534|4625|帳戶登入失敗|
|535|4625|帳戶登入失敗|
|536|4625|帳戶登入失敗|
|537|4625|帳戶登入失敗|
|539|4625|帳戶登入失敗|

## Windows排程管理員
## Linux系統指令
## lucene 語法
## elasticsearch DSL 語法
