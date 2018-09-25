# Information-security
## 目錄

* [Windows事件檢視器](#windows事件檢視器)

* [Windows排程管理員](#windows排程管理員)

* [Linux系統指令](#linux系統指令)

* [lucene 語法](#lucene-語法)

* [elasticsearch DSL 語法](#elasticsearch-dsl-語法)

* [Reference](#reference)

## Windows事件檢視器

開始 → 執行 → 輸入 eventvwr 開啟事件檢視器

### Event Log
----
|Event ID|Description|Event ID|Description|
|:----:|:----|:----:|:----|
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

### Logon/Logoff event difference
----
```
Group A : Windows 2003 and before

Group B : Windows 2008 R2 and Windows 7 , Windows 2012 R2 and Windows 8.1 , Windows 2016 and Windows 10
```
|Group A event ID|Group B event ID|Description|
|:---:|:---:|:---|
|528|4624|帳戶成功登入|
|540|4624|帳戶成功登入|
|538|4634|帳戶已經登出|
|551|4647|帳戶已經登出|
|529|4625|帳戶登入失敗，有人使用未知的使用者名稱或密碼錯誤的已知使用者名稱來試圖登入|
|530|4625|帳戶登入失敗，試圖登入的使用者帳戶是在非法時間進行登入|
|531|4625|帳戶登入失敗，有人使用已停用的帳戶試圖登入|
|532|4625|帳戶登入失敗，有人使用過期的帳戶試圖登入|
|533|4625|帳戶登入失敗，系統不允許這個使用者登入這部電腦|
|534|4625|帳戶登入失敗，使用者試圖以不被允許的登入類型來進行登入，例如透過網路、互動式、批次、服務或遠端互動式|
|535|4625|帳戶登入失敗，指定的帳戶密碼已經過期|
|536|4625|帳戶登入失敗，沒有啟用 Net Logon 服務|
|537|4625|帳戶登入失敗，登入意圖因其他原因而失敗|
|539|4625|帳戶登入失敗，此帳戶在試圖登入時被鎖定。此事件可能暗示有人發動密碼攻擊，但沒有成功因而造成此帳戶被鎖定|

### Logon event type
----
|Type|Title|Description|
|:----:|:----|:----|
|2|互動|使用者已登入這部電腦|
|3|網路|使用者或電腦從網路登入這部電腦|
|4|批次|批次登入類型會使用批次的伺服器，代表其直接介入使用者執行處理程序可能地方|
|5|服務|服務已啟動的服務控制管理員|
|7|解除鎖定|輸入密碼登入使工作站解除鎖定|
|10|RemoteInteractive|使用者使用[終端機服務]或[遠端桌面]從遠端登入這部電腦|

### Account management
----
```
Group A : Windows 2003 and before

Group B : Windows 2008 R2 and Windows 7 , Windows 2012 R2 and Windows 8.1 , Windows 2016 and Windows 10
```
|Group A event ID|Group B event ID|Description|
|:----:|:----:|:----|
|624|4720|已建立使用者帳戶|
|625|None|已變更使用者帳戶類型|
|626|4722|已啟用使用者帳戶|
|627|4723|有人試圖變更密碼|
|628|4724|已設定使用者帳戶密碼|
|629|4725|已停用使用者帳戶|
|630|4726|已刪除使用者帳戶|
|631|4727|已建立安全性啟用的通用群組|
|632|4728|已新增安全性啟用的通用群組成員|
|633|4729|已移除安全性啟用的通用群組成員|
|634|4730|已刪除安全性啟用的通用群組|
|635|4731|已建立安全性停用的本機群組|
|636|4732|已新增安全性啟用的本機群組成員|
|637|4733|已移除安全性啟用的本機群組成員|
|638|4734|已刪除安全性啟用的本機群組|
|639|4735|已變更安全性啟用的本機群組|
|641|4737|已變更安全性啟用的通用群組|
|642|4738|已變更使用者帳戶|
|643|4739|已變更網域原則|
|644|4740|已鎖定使用者帳戶|


## Windows排程管理員
## Linux系統指令
### Linux系統架構
----
|Path|Description|
|:----:|:----|
|/bin|放置一般使用者可以操作的指令，路徑為/usr/bin|
|/sbin|放置系統管理員可以操作的指令，路徑為/usr/sbin|
|/boot|放置開機相關檔案|
|/dev|放置 device 裝置檔案|
|/etc|放置系統檔案|
|/home|一般帳戶的家目錄|
|/root|系統管理者的家目錄|
|/lib|系統函式庫和核心函式庫，路徑為/usr/lib|
|/lib64|系統64位元的系統函式庫和核心函式庫，路徑為/usr/lib64|
|/proc|將記憶體內的資料做成檔案類型|
|/sys|與/proc類似，但主要針對硬體相關參數|
|/usr|全名為unix software resource縮寫，放置系統相關軟體、服務|
|/var|全名為 variable，放置一些變數或記錄檔|
|/tmp|全名為 temporary，放置暫存檔案|
|/media|放置隨插即用的裝置慣用目錄|
|/mnt|為管理員/使用者手動掛上安裝（mount）的目錄|
|/opt|全名為 optional，通常為第三方廠商放置軟體處|
|/run|系統進行服務軟體運作管理處|
|/srv|通常是放置開發的服務（service），如：網站服務www等|
### 檔案與目錄管理指令
----
|Command|Description|
|:----:|:----|
|ls|查看檔案及子目錄|

列出目錄基本資料
```
$ ls
```
列出目錄詳細資料
```
$ ls -l
```
列出目錄隱藏資料
```
$ ls -a
```
列出目錄部分資料
例:列出為副檔名為.jpg的檔案
```
$ ls *.jpg
```
----
|Command|Description|
|:----:|:----|
|pwd|print work directory，印出目前工作目錄|

----
|Command|Description|
|:----:|:----|
|cd|change directory，切換至目錄|

切換至當前目錄下的examples目錄
```
$ cd ./examples
```
切換至家目錄
```
$ cd ~
```
切換至上一層目錄
```
$ cd ..
```
切換至根目錄
```
$ cd /
```
----
|Command|Description|
|:----:|:----|
|mkdir|make directory，創建新資料夾|

創建examples資料夾
```
$ mkdir examples
```
----
|Command|Description|
|:----:|:----|
|cp|copy，複製檔案|

----
|Command|Description|
|:----:|:----|
|mv|copy，move(rename) files，移動檔案或是重新命名檔案|

移動檔案
例:將README.md移至/examples/目錄下
```
$ mv README.md /examples/README.md
```
重新命名
例:將README.md重新命名為README_1
```
$ mv README.md README_1.md
```
----
|Command|Description|
|:----:|:----|
|rm|remove file，刪除檔案|

刪除當前目錄下副檔名為.jpg的檔案
```
$ rm *.jpg
```
刪除examples資料夾和所有檔案
```
$ rm -f examples
```
----
|Command|Description|
|:----:|:----|
|touch|用來更新已存在文件的時間戳記(timestamp)或是新增空白檔案|

----
|Command|Description|
|:----:|:----|
|cat|將文件印出在終端機上|

----
|Command|Description|
|:----:|:----|
|tail|顯示檔案最後幾行內容|

持續顯示更新內容
```
$ tail -f README.md
```
----
|Command|Description|
|:----:|:----|
|more|將檔案一頁頁印在終端機上|

----
|Command|Description|
|:----:|:----|
|file|檢查檔案類型|

### 檔案權限
----
檢視檔案權限可以使用 $ ls -l 來查看
```
 $ ls -l
 total 220
 drwxr-xr-x  22   root   root   4096   May 4 18:01 .config
 -rw-r--r--   1   root   root   1864   May 7 15:05 initial-setup-ks.cfg
 ...
```
* 第一欄:檔案的類型與權限
由 10 個字元組成

  * 第一個字元表示檔案型態

    * [ - ] 為檔案，如上表檔名為 initial-setup-ks.cfg

    * [ d ] 為目錄，如上表檔名為 .config

    * [ l ] 為連結檔案(link file)

    * [ b ] 為裝置檔裡面的可供儲存的周邊設備(可隨機存取裝置)

    * [ c ] 為裝置檔裡面的序列埠設備，例如鍵盤、滑鼠(一次性讀取裝置)

字元 2、3、4 表示檔案擁有者的存取權限。字元 5、6、7 表示檔案擁有者所屬群組成員的存取權限。字元 8、9、10 表示其他使用者的存取權限
## lucene 語法
## elasticsearch DSL 語法
## Reference
[稽核登入事件](https://docs.microsoft.com/zh-tw/windows/security/threat-protection/auditing/basic-audit-logon-events)
