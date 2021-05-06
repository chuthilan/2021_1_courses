# 常用Powershell 小指令(cmdlets)
```
完成底下Powershell 小指令(cmdlets)的測試報告
```
# 1
```
Get-ExecutionPolicy   


Unrestricted
```

```
Set-ExecutionPolicy Unrestricted

```

# Get-help 
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


```
Get-Help
Get-ExecutionPolicy   Set-ExecutionPolicy

Get-ChildItem ==> Enumerating Files, Folders, and Registry Keys
  Get-Command -Name Get-ChildItem -Syntax

ConvertTo-HTML
Export-CSV


系統
Get-Process  Stop-Process
Get-Service
Get-Member
Get-EventLog


網路

registry


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
