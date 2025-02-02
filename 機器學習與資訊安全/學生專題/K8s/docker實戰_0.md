#
```
Docker + Kubernetes 應用開發與快速上雲
李文強著   機械工業   2020-04-01
https://www.3dwoo.com/showBookDetail.asp?nb=52549

https://github.com/xin-lai/docker-k8s
```

```
第1章 走進Docker1
1.1 主流的互聯網公司均在使用Docker1
1.2 什麼是Docker4
1.3 容器簡史4
1.4 打消偏見，迎接Docker5
1.5 Docker和虛擬機6
1.6 Docker的三個基本概念8
1.6.1 鏡像：一個特殊的檔系統8
1.6.2 容器：鏡像運行時的實體9
1.6.3 倉庫：集中存放鏡像檔的地方9
1.7 Docker版本概述11


第2章 Docker的市場趨勢和主要應用場景12
2.1 Docker的市場趨勢12
2.2 Docker的主要應用場景15
2.2.1 簡化配置，無須處理復雜的環境依賴關系15
2.2.2 搭建輕量、私有的PaaS環境、標準化開發、測試和生產環境15
2.2.3 簡化和標準化代碼流水線，助力敏捷開發和DevOps實踐16
2.2.4 隔離應用17
2.2.5 整合服務器資源17
2.2.6 現代應用17
2.2.7 調試能力18
2.2.8 快速部署18
2.2.9 混合雲應用、跨環境應用、可移植應用18
2.2.10 物聯網和邊緣計算18


第3章 安裝和運行20
3.1 Windows 10下的安裝20
3.1.1 配置Docker本地環境22
3.1.2 運行一個簡單的demo23

3.2 Ubuntu下的安裝25
3.2.1 瞭解Ubuntu25
3.2.2 使用Hyper-V快速安裝Ubuntu25
3.2.3 配置外網27
3.2.4 使用SSH遠程Ubuntu30
3.2.5 安裝Docker33

3.3 CentOS 下的安裝37
3.3.1 瞭解CentOS37
3.3.2 使用CentOS 7 安裝Docker38

3.4 基於樹莓派搭建個人網盤41
3.4.1 什麼是樹莓派41
3.4.2 開啟SSH43
3.4.3 安裝Docker44
3.4.4 基於樹莓派的一行命令搭建個人網盤46


第4章 Docker命令基礎知識48
4.1 登 錄49
4.1.1 OPTIONS說明49
4.1.2 登錄Docker Hub49
4.1.3 登錄到騰訊雲鏡像倉庫50
4.2 拉取鏡像51
4.2.1 OPTIONS說明51
4.2.2 從Docker Hub拉取鏡像51
4.2.3 從騰訊雲鏡像倉庫拉取鏡像52
4.3 列出本地鏡像53
4.3.1 OPTIONS說明53
4.3.2 按名稱和標簽列出鏡像54
4.3.3 篩選55
4.4 運行鏡像58
4.4.1 OPTIONS說明58
4.4.2 簡單運行60
4.5 列出容器61
4.5.1 OPTIONS說明61
4.5.2 查看正在運行的容器61
4.5.3 顯示正在運行和已停止的容器61
4.5.4 篩選62
4.5.5 根據**範本輸出62
4.6 查看鏡像詳情63

4.7 刪除鏡像64
4.7.1 OPTIONS說明64
4.7.2 批量刪除65

4.8 清理未使用的鏡像65
4.9 磁盤佔用分析67
4.10 刪除容器68
4.10.1 OPTIONS說明68
4.10.2 停止容器再刪除68
4.10.3 強制刪除正在運行的容器69
4.10.4 刪除所有已停止的容器69
4.11 鏡像構建70
4.11.1 OPTIONS說明70
4.11.2 簡單構建71
4.12 鏡像歷史73
4.12.1 OPTIONS說明73
4.12.2 查看鏡像歷史74
4.12.3 格式化輸出74
4.13 修改鏡像名稱和標簽75
4.14 鏡像推送76
4.14.1 推送到Docker Hub76
4.14.2 推送到騰訊雲鏡像倉庫77
4.15 使用Kitematic來管理Docker容器77


第5章 Docker持續開發工作流81
5.1 基於Docker容器的內部循環開發工作流81
5.1.1 開發82
5.1.2 編寫Dockerfile83
5.1.3 創建自定義鏡像90
5.1.4 定義docker-compose91
5.1.5 啟動Docker應用97
5.1.6 測試99
5.1.7 部署或繼續開發100


5.2 Visual Studio和Docker100
5.2.1 使用VS自動生成工程的Dockerfile檔101
5.2.2 VS支援的容器業務協調程式102
5.2.3 使用VS發布鏡像104

5.3 使用 Visual Studio Code玩轉Docker105
5.3.1 官方擴展外掛程式Docker105
5.3.2 Docker Compose擴展外掛程式109


第6章 Docker應用開發之旅111
6.1 使用.NET Core開發雲原生應用111
6.1.1 什麼是“雲原生”112
6.1.2 .NET Core簡介112
6.1.3 官方鏡像114
6.1.4 Kestrel115
6.1.5 按環境加載配置118
6.1.6 查看和設置容器的環境變量119
6.1.7 ASP.NET Core內置的日誌記錄提供程式121
6.1.8 編寫一個簡單的Demo輸出日誌122
6.1.9 使用“docker logs”查看容器日誌124
6.1.10 使用“docker stats”查看容器資源使用125
6.1.11 如何解決容器應用的時區問題125

6.2 使用Docker搭建Java開發環境127
6.2.1 官方鏡像127
6.2.2 使用Docker搭建Java開發環境127
6.2.3 Docker資源限制130
6.2.4 防止Java容器應用被殺130

6.3 使用Go推送釘釘消息131
6.3.1 Go的優勢131
6.3.2 官方鏡像132
6.3.3 使用Go推送釘釘消息133

6.4 使用Python實現簡單爬蟲140
6.4.1 關於Python140
6.4.2 官方鏡像140
6.4.3 使用Python抓取博客列表141


6.5 使用PHP搭建個人博客站點145
6.5.1 官方鏡像146
6.5.2 編寫簡單的“Hello world”146
6.5.3 使用WordPress鏡像搭建個人博客站點148
6.5.4 修改PHP的檔上傳大小限制151

6.6 使用Node.js搭建團隊技術文檔站點151
6.6.1 官方鏡像152
6.6.2 編寫一個簡單的Web服務器152
6.6.3 使用Hexo搭建團隊技術文檔站點154


第7章 數據庫容器化161
7.1 什麼是數據庫161
7.2 關系型數據庫和非關系型數據庫對比162
7.3 主流的數據庫162
7.4 數據庫容器化163

7.5 SQL Server容器化163
7.5.1 鏡像說明164
7.5.2 運行SQL Server 容器鏡像165
7.5.3 管理SQL Server168

7.6 如何持久保存數據174
7.6.1 方式一：使用主機目錄175
7.6.2 方式二：使用數據卷178

7.7 MongoDB容器化179
7.7.1 適用場景179
7.7.2 不適用場景180
7.7.3 鏡像說明180
7.7.4 運行MongoDB容器鏡像180
7.7.5 管理MongoDB181

7.8 Redis容器化184
7.8.1 優勢184
7.8.2 運行Redis鏡像185
7.8.3 使用redis-cli185
7.8.4 使用Redis Desktop Manager管理Redis186
7.8.5 既好又快地實現排行榜187

7.9 MySQL容器化191
7.9.1 鏡像說明191
7.9.2 運行MySQL容器鏡像192
7.9.3 管理MySQL194


第8章 搭建Kubernetes集群198
8.1 Docker+ Kubernetes已成為雲計算的主流198
8.1.1 什麼是Kubernetes198
8.1.2 Kubernetes正在塑造應用程式開發和管理的未來199
8.2 Kubernetes主體架構199
8.2.1 主要核心組件200
8.2.2 基本概念202

8.3 使用Minikube部署本地Kubernetes集群208
8.3.1 什麼是Kubernetes集群208
8.3.2 使用Minikube創建本地Kubernetes實驗環境209

8.4 使用kubectl管理Kubernetes集群217
8.4.1 概述217
8.4.2 語法217
8.4.3 主要命令說明218
8.4.4 資源類型說明220
8.4.5 命令標志說明221
8.4.6 格式化輸出221

8.5 使用kubeadm創建集群222
8.5.1 kubeadm概述222
8.5.2 kubelet概述223
8.5.3 定義集群部署目標和規劃223
8.5.4 開始部署224
8.5.5 主節點部署229
8.5.6 工作節點部署237
8.5.7 安裝儀表盤239

8.6 集群故障處理243
8.6.1 健康狀態檢查——初診244
8.6.2 進一步診斷分析——聽診三板斧247
8.6.3 容器調測252
8.6.4 對癥下藥254
8.6.5 部分常見問題處理255
8.6.6 小結260

第9章 將應用部署到Kubernetes集群261
9.1 使用kubectl部署應用261
9.1.1 kubectl部署流程261
9.1.2 部署一個簡單的Demo網站262

9.2 應用伸縮和回滾264
9.2.1 使用“kubectl scale”命令來伸縮應用264
9.2.2 使用“kubectl autoscale”命令來自動伸縮應用265
9.2.3 使用“kubectl run”命令快速運行應用265
9.2.4 使用“kubectl set”命令*新應用266
9.2.5 使用“kubectl rollout”命令回滾應用268

9.3 通過Service訪問應用269
9.3.1 通過Pod IP訪問應用269
9.3.2 通過ClusterIP Service在集群內部訪問270
9.3.3 通過NodePort Service在外部訪問集群應用272
9.3.4 通過LoadBalancer Service在外部訪問集群應用274
9.3.5 Microsoft SQL Server數據庫實戰276

9.4 使用Ingress負載分發微服務278
9.4.1 Demo規劃279
9.4.2 準備Demo並完成部署279
9.4.3 創建部署資源280
9.4.4 創建服務資源282
9.4.5 創建Ingress資源並配置轉發規則283

9.5 利用Helm簡化Kubernetes應用部署286
9.5.1 Helm基礎287
9.5.2 安裝Helm287
9.5.3 使用Visual Studio 2019為Helm編寫一個簡單的應用289
9.5.4 定義charts293
9.5.5 使用Helm部署Demo296
9.5.6 Helm常用操作命令301


**0章 將應用託管到雲端303
10.1 什麼是雲計算303
10.1.1 為什麼要上雲304
10.1.2 雲計算的三種部署方式305
10.1.3 雲服務的類型305
10.2 Docker+k8s是上雲的***306
10.2.1 上雲的問題306
10.2.2 利用Docker+k8s解決傳統應用上雲問題306

10.3 主流雲計算容器服務介紹307
10.3.1 ***AWS307
10.3.2 微軟Azure308
10.3.3 阿裡雲310
10.3.4 騰訊雲311

10.4 自建還是託管312
10.4.1 自建容器服務存在的問題312
10.4.2 雲端容器服務的優勢313

10.5 一般應用服務部署流程313
10.5.1 創建集群和節點314
10.5.2 創建命名空間和鏡像314
10.5.3 創建服務317
10.5.4 配置鏡像觸發器323
10.5.5 推送鏡像324

10.6 如何節約雲端成本325
10.6.1 無須過度購買配置，盡量使用自動擴展325
10.6.2 *大化地利用服務器資源325
10.6.3 使用Ingress節約負載均衡資源326
10.6.4 使用NFS盤節約存儲成本327

10.7 問題處理327
10.7.1 鏡像拉取問題327
10.7.2 綁定雲硬盤之後Pod的調度問題329
10.7.3 遠程登錄329
10.7.4 利用日誌來排查問題330


**1章 容器化後DevOps之旅332
11.1 DevOps基礎知識332
11.1.1 什麼是DevOps332
11.1.2 為什麼需要DevOps333
11.1.3 DevOps對應用程式發布的影響335
11.1.4 如何實施DevOps335

11.2 Docker與持續集成和持續部署336
11.2.1 Docker與持續集成和持續部署336
11.2.2 參考流程338

11.3 使用Azure DevOps完成CI/CD340
11.3.1 適用於容器的CI/CD流程341
11.3.2 使用Azure DevOps配置一個簡單的CI/CD流程341

11.4 使用Tencent Hub完成CI/CD347
11.4.1 關於Tencent Hub347
11.4.2 使用Tencent Hub配置一個簡單的CI流程348
11.4.3 直接使用容器服務的鏡像構建功能360

11.5 使用內部管理工具完成CI/CD流程361
11.5.1 一個簡單的CI/CD流程361
11.5.2 關於TeamCity361
11.5.3 運行TeamCity Server363
11.5.4 運行TeamCity Agent364
11.5.5 連接和配置Agent366
11.5.6 創建項目以及配置CI367
11.5.7 使用Jenkins完成CI/CD372
```
