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
|261|連線接收|4647|使用者啟動的登出|
|1100|Windows已停止事件紀錄|4648|帳戶成功登入|
|1101|事件在傳輸過程被丟棄|4657|修改Registry value|
|1102|事件紀錄檔已被清除|4697|安裝新的服務|
|1149|授權成功|4688|已建立新的處理程序|
|4104|執行Remote Command|4720|使用者帳戶已被成功創建|
|4624|帳戶成功登入|4724|您嘗試重設帳戶密碼|
|4625|帳戶登入失敗|7034|服務無預期關閉|
|4634|帳戶已經登出|7036|服務啟動或是關閉|
|4638|帳戶成功登入|7040|服務啟動模式改變|

### Logon event type
---------------
|Type|Title|Description|
|:--:|:----|:----------|
|2|互動|使用者已登入這部電腦|
|3|網路|使用者或電腦從網路登入這部電腦|
|7|解除鎖定|輸入密碼登入使工作站解除鎖定|
|10|RemoteInteractive|使用者使用[終端機服務]或[遠端桌面]從遠端登入這部電腦|

## Windows排程管理員
## Linux系統指令
## lucene 語法
## elasticsearch DSL 語法
