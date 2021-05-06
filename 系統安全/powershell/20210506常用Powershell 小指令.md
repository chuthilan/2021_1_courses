# 常用Powershell 小指令(cmdlets)
```
完成底下Powershell 小指令(cmdlets)的測試報告
```
# 1 ExecutionPolicy 執行原則
```
檢視方式 ==> 
Get-ExecutionPolicy   
```
```
Unrestricted
```

```
設定方式 ==> 
Set-ExecutionPolicy Unrestricted
```
```
執行原則 ==> 有下列 4 種：
Restricted ：關閉腳本檔的執行功能，這是預設的設定值。
AllSigned ：只允許執行受信任發行者簽署過的腳本檔。
RemoteSigned ：在本機電腦所撰寫的腳本檔，不需要簽署就可執行；
     但是從網際網路（例如：email、MSN Messenger）下載的腳本檔就必須經過受信任發行者的簽署才能執行。
Unrestricted ：任何腳本檔皆可被執行，但是於執行網際網路下載的腳本檔時，會先出現警告的提示視窗。
```

# 2.Get-help 
## 收集電腦的相關資訊Get-CimInstance
```
https://docs.microsoft.com/zh-tw/powershell/scripting/samples/collecting-information-about-computers?view=powershell-7.1
```
```
PS C:\Users\owner> get-help Get-CimInstance

NAME
    Get-CimInstance

SYNTAX
    Get-CimInstance [-ClassName] <string> [-ComputerName <string[]>] [-KeyOnly] [-Namespace <string>]
    [-OperationTimeoutSec <uint32>] [-QueryDialect <string>] [-Shallow] [-Filter <string>] [-Property <string[]>]
    [<CommonParameters>]

    Get-CimInstance [-InputObject] <ciminstance> -CimSession <CimSession[]> [-ResourceUri <uri>] [-OperationTimeoutSec
    <uint32>]  [<CommonParameters>]

    Get-CimInstance -CimSession <CimSession[]> -Query <string> [-ResourceUri <uri>] [-Namespace <string>]
    [-OperationTimeoutSec <uint32>] [-QueryDialect <string>] [-Shallow]  [<CommonParameters>]

    Get-CimInstance [-ClassName] <string> -CimSession <CimSession[]> [-KeyOnly] [-Namespace <string>]
    [-OperationTimeoutSec <uint32>] [-QueryDialect <string>] [-Shallow] [-Filter <string>] [-Property <string[]>]
    [<CommonParameters>]

    Get-CimInstance -CimSession <CimSession[]> -ResourceUri <uri> [-KeyOnly] [-Namespace <string>]
    [-OperationTimeoutSec <uint32>] [-Shallow] [-Filter <string>] [-Property <string[]>]  [<CommonParameters>]

    Get-CimInstance -ResourceUri <uri> [-ComputerName <string[]>] [-KeyOnly] [-Namespace <string>]
    [-OperationTimeoutSec <uint32>] [-Shallow] [-Filter <string>] [-Property <string[]>]  [<CommonParameters>]

    Get-CimInstance [-InputObject] <ciminstance> [-ResourceUri <uri>] [-ComputerName <string[]>] [-OperationTimeoutSec
    <uint32>]  [<CommonParameters>]

    Get-CimInstance -Query <string> [-ResourceUri <uri>] [-ComputerName <string[]>] [-Namespace <string>]
    [-OperationTimeoutSec <uint32>] [-QueryDialect <string>] [-Shallow]  [<CommonParameters>]


ALIASES
    gcim


REMARKS
    Get-Help cannot find the Help files for this cmdlet on this computer. It is displaying only partial help.
        -- To download and install Help files for the module that includes this cmdlet, use Update-Help.
        -- To view the Help topic for this cmdlet online, type: "Get-Help Get-CimInstance -Online" or
           go to https://go.microsoft.com/fwlink/?LinkId=227961.


```

# 3.使用檔案及資料夾
```
https://docs.microsoft.com/zh-tw/powershell/scripting/samples/working-with-files-and-folders?view=powershell-7.1


Get-ChildItem 

```
```
https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.management/get-childitem?view=powershell-7.1
```
```
Get-ChildItem ==> Enumerating Files, Folders, and Registry Keys
  Get-Command -Name Get-ChildItem -Syntax

ConvertTo-HTML
Export-CSV

```
# 適用於系統管理的範例指令碼
```
https://docs.microsoft.com/zh-tw/powershell/scripting/samples/sample-scripts-for-administration?view=powershell-7.1
```
##  使用物件
```
檢視物件結構 - Get-Member
選取物件的組件 - Select-Object
從管線中移除物件 - Where-Object

為物件排序
對多個物件重複工作 - ForEach-Object
建立 .NET 和 COM 物件 - New-Object
使用靜態類別和方法
取得 WMI 物件 - Get-CimInstance
```
## 管理電腦
```
變更電腦狀態
收集電腦的相關資訊
使用 FilterHashtable 建立 Get-WinEvent 查詢
```
# 管理處理序與服務
```
使用 FilterHashtable 建立 Get-WinEvent 查詢
使用處理序 Cmdlet 管理處理序
管理服務
管理 PowerShell 磁碟機
使用印表機
執行網路工作
處理軟體安裝
從正在執行的處理序解碼 PowerShell 命令
```
## 使用輸出
```
使用 Out-* Cmdlet 將資料重新導向
使用格式命令變更輸出檢視
```
## 管理裝置與檔案
```
管理目前的位置
使用檔案及資料夾
使用檔案、資料夾與登錄機碼
使用登錄項目
使用登錄機碼
```
## 建立UI元素
```
建立自訂輸入方塊
建立圖形化日期選擇器
多重選取清單方塊
從清單方塊選取項目
```
## 其他範例
```
直接操作項目
其他實用的指令碼物件
附錄 1 相容性別名
附錄 2 建立自訂 PowerShell 捷徑
```
# 行程管理
```
Get-Process  Stop-Process
Get-Service
Get-Member
Get-EventLog
```

# 網路

# registry

```
Windows Management Instrumentation (WMI) 

Get-CimInstance ==>

COM
New-Object ==> 建立 .NET and COM Objects
```
```
Sample scripts for system administration
https://docs.microsoft.com/en-us/powershell/scripting/samples/sample-scripts-for-administration?view=powershell-7.1

https://www.techrepublic.com/blog/10-things/10-powershell-commands-every-windows-admin-should-know/
```
