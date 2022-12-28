# mypkg
![test](https://github.com/rikuhotakeda/mypkg/actions/workflows/test.yml/badge.svg)

仮talkerノードからcountupというトピックで数字のメッセージをlistenerノードへ受け渡しする。

## 必要なソフトウェア
* Python 3.10
* Ubuntu 22.04

## 使い方
### 環境準備
* ワークスペースを作成し移動する。
```
$ mkdir -p ros2_ws/src
$ cd ~/ros2_ws/src
```

* `git clone`を使って本パッケージをダウンロードする。
```
$ git clone https://github.com/rikuhotakeda/mypkg
```

* パッケージを利用可能にするため、~/.bashrcの末尾に以下の2行を追加する。
```
source ~/ros2_ws/install/setup.bash
source ~/ros2_ws/install/local_setup.bash
```

### 実行例
ros2_wsのディレクトリに移動する。
```
cd ~/ros2/src
```

ローンチファイルを用いてtalkerros
