# kubernetes勉強会
## （基本編）

---

### kubernetes(k8s)とは？
- Kubernetes はコンテナ化されたアプリケーションのデプロイ、スケーリングなどの管理を自動化するためのプラットフォーム（コンテナオーケストレーションエンジン）です。

---

### コンテナとは？
- OS上に「独立したサーバーと同様の振る舞いをする区画」のこと。  
  カーネルなどの機能を使って、OSのプロセスとして起動する。

- **※ LinuxOSのコンテナでWindowsのアプリは動かない！**

--- 

### Dockerコンテナ
![Dockerコンテナ](http://image.itmedia.co.jp/ait/articles/1701/30/wi-docker01002.png)
http://image.itmedia.co.jp/ait/articles/1701/30/wi-docker01002.png

---

# コンテナ ≒ 仮想ホスト（VM） 

+++

### 参考
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

![k8sアーキ](https://www.google.co.jp/url?sa=i&source=images&cd=&cad=rja&uact=8&ved=2ahUKEwih4NKei-DfAhVUdt4KHf6CAj4QjRx6BAgBEAU&url=https%3A%2F%2Fqiita.com%2Ftkusumi%2Fitems%2Fc2a92cd52bfdb9edd613&psig=AOvVaw3rNoGCCjKTWJYklaILWOm3&ust=1547102247066467)

---

### kubernetes 
- Workloads リソースコンテナの実行に関するリソース
- Discovery ＆ LB リソースコンテナを外部公開するようなエンドポイントを提供するリソース
- Config ＆ Storage リソース設定／機密情報／永続化ボリュームなどに関するリソース
- Cluster リソースセキュリティやクォータなどに関するリソース
- Metadata リソースクラスタ内の他のリソースを操作するためのリソース

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

  +++
### Pods-overview
- https://kubernetes.io/docs/tutorials/kubernetes-basics/explore/explore-intro/#pods-overview

![pods-overview](https://d33wubrfki0l68.cloudfront.net/fe03f68d8ede9815184852ca2a4fd30325e5d15a/98064/docs/tutorials/kubernetes-basics/public/images/module_03_pods.svg)


### Node-overview
- https://kubernetes.io/docs/tutorials/kubernetes-basics/explore/explore-intro/#node-overview

![node-overview](https://kubernetes.io/docs/tutorials/kubernetes-basics/explore/explore-intro/#node-overview)