# Statistics : 統計学基礎
- Python による実装

  - python で実際の data を統計解析をする

## 環境構築
- Docker & JupyterLab

- [docker 環境構築詳細](document/devlopment_manual.md#anchor1)

  - **document / development_manual.md 参照**

### Docker の基本操作
### docker pull
    docker pull datascientistus/ds-python-env2
### docker image 一覧表示
    docker images
### docker image から container 起動
    docker run -v ~Dropbox/udemy/statistics:/work -p 1212:8888 --name st-env datascientistus/ds-python-env2
- 今回は `1212:8888` という `port` の上で動くようにしてある `default の Jupyter の port の番号は 8888`
- container の　**port を Host に繋げてあげないと動かない。**　なので host 側の localhost.`1212` に接続すると container `8888` に届くようになっている
### container 一覧表示
    docker ps -a
### container を止める
    docker stop <container>
### container を削除
    docker rm <container>
### container image 削除
    docker rmi <image id>
### container restart
    docker restart <container>
