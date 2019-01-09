# kubernetes勉強会
## （基本編）

---

### kubernetes(k8s)とは？
- Kubernetes は**コンテナ化されたアプリケーション**のデプロイ、スケーリングなどの管理を自動化するためのプラットフォーム（コンテナオーケストレーションエンジン）です。

---

### コンテナとは？
- OS上に「独立したサーバーと同様の振る舞いをする区画」のこと。  
  カーネルなどの機能を使って、OSのプロセスとして起動する。

@box[bg-orange text-white rounded demo-box-pad](LinuxOSのコンテナでWindowsのアプリは動かない！)

--- 

### Dockerコンテナ
![Dockerコンテナ](http://image.itmedia.co.jp/ait/articles/1701/30/wi-docker01002.png)
http://image.itmedia.co.jp/ait/articles/1701/30/wi-docker01002.png

---

### コンテナ ≒ 仮想ホスト（VM） 

+++

### 参考
#### DockreFileの書き方を学ぶ
- 改めてDockerfileのベストプラクティスを振り返ろう
  https://www.slideshare.net/ssuser1f3c12/introduce-that-best-practices-for-writing-dockerfiles

---

### k8sで何ができるか？
  - 複数のKubernetes Node の管理
  - コンテナのスケジューリング
  - ローリングアップデート
  - スケーリング／オートスケーリング
  - コンテナの死活監視
  - 障害時のセルフヒーリング
  - サービスディスカバリ
  - ロードバランシング
  - データの管理
  - ワークロードの管理
  - ログの管理
  - Infrastructure as Code
  - その他エコシステムとの連携や拡張 (下ページ）

+++

### エコシステム  

![エコシステム](https://landscape.cncf.io/format=landscap)

---

### アーキテクチャ

![k8sアーキ](https://camo.qiitausercontent.com/c2d6e9c630a7fcfcbb6638f104d1718e7e603276/68747470733a2f2f71696974612d696d6167652d73746f72652e73332e616d617a6f6e6177732e636f6d2f302f3130303337372f38333032633861362d383361322d333633312d613662342d3762643535356433613138622e706e67)

---

### kubernetes 
- Workloads
  リソースコンテナの実行に関するリソース
- Discovery ＆ LB
  リソースコンテナを外部公開するようなエンドポイントを提供するリソース
- Config ＆ Storage
  リソース設定／機密情報／永続化ボリュームなどに関するリソース
- Cluster
  リソースセキュリティやクォータなどに関するリソース
- Metadata
  リソースクラスタ内の他のリソースを操作するためのリソース

---

### kubernetes リソース
- Workloads
  - Pod
  - ~~ReplicationController~~
  - ReplicaSet
  - Deployment
  - DaemonSet
  - StatefulSet
  - Job
  - CronJob

---

### Workloadsの階層構造
- Pod  ---> ReplicaSet  ---> Deployment 
- Pod  ---> DemonSet
- Pod  ---> StatefulSet
- Pod  ---> Job         ---> CronJob

---

### Pods-overview
- https://kubernetes.io/docs/tutorials/kubernetes-basics/explore/explore-intro/#pods-overview

![pods-overview](https://d33wubrfki0l68.cloudfront.net/fe03f68d8ede9815184852ca2a4fd30325e5d15a/98064/docs/tutorials/kubernetes-basics/public/images/module_03_pods.svg)

---

### Node-overview
- https://kubernetes.io/docs/tutorials/kubernetes-basics/explore/explore-intro/#node-overview

![node-overview](https://d33wubrfki0l68.cloudfront.net/5cb72d407cbe2755e581b6de757e0d81760d5b86/a9df9/docs/tutorials/kubernetes-basics/public/images/module_03_nodes.svg)

---

終わり
