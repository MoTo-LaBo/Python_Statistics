# Statistics : 統計学基礎
- Python による実装

  - python で実際の data を統計解析をする
### 統計学
1. **記述統計**
   - 1-1. [data set](01_descriptive_st/00_data_set.ipynb)

   - 1-2. [分布 (distribution)](01_descriptive_st/01_distribution.ipynb)

   - 1-3. [記述・推測統計(代表値：平均値・中央値・最頻値)](01_descriptive_st/02_des_inf_st.ipynb)

   - 1-4. [散布度]()

2. **２変数関数の記述統計**

3. 確率

4. [正規分布と標準化]()

5. [推測統計入門]()

6. [区間推定]()

7. [統計的仮説検定]()

8. [２群の比率差の検定(z検定)]()

9.  [連関の検定(カイニ乗検定)]()

10. [２群の平均値差の検定(t検定)]()

11. [正規性と等分散性の検定]()

12. [対応ありの平均値差の検定]()

13. [検定の誤りと検定力]()

14. [検定力分析]()

## 環境構築
- Docker & JupyterLab

- [docker 環境構築詳細](document/devlopment_manual.md#anchor1)

  - **document / development_manual.md 参照**

### Docker の基本操作
### docker pull
    docker pull datascientistus/ds-python-en2
- **実際 pull はいらない！笑**
  - 形式として、一連の流れてして一応覚えておく

  - `docker run ...` の command 1行を入力するれば自動で　**datascientistus/ds-python-env2　を pull してくれる**
### docker image 一覧表示
    docker images
### docker image から container 起動
    docker run -v ~/Dropbox/udemy/statistics:/work -p 1212:8888 --name st-env datascientistus/ds-python-env2
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
