# title
![test](https://github.com/rikuhotakeda/mypkg/actions/workflows/test.yml/badge.svg)

talkerノードからcountupというトピックで数字のメッセージをlistenerノードへ受け渡しする。

* ros2のパッケージです。

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

* `git clone`を使ってパッケージをダウンロードする。
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

* [talker](https://github.com/rikuhotakeda/mypkg/blob/master/mypkg/talker.py)と[listener](https://github.com/rikuhotakeda/mypkg/blob/master/mypkg/listener.py)の実行例
```
端末１$ ros2 run mypkg talker.py
端末２$ ros2 run mypkg lisetener.py
[INFO] [1672236118.622220183] [listener]: Listen: 36
[INFO] [1672236119.093162568] [listener]: Listen: 37
[INFO] [1672236119.593843579] [listener]: Listen: 38
```

* [launch_talk.launch.py](https://github.com/rikuhotakeda/mypkg/blob/master/launch/talk_listen.launch.py)ローンチファイルでの実行例
```
$ ros2 launch mypkg talk_listen.launch.py
[INFO] [launch]: All log files can be found below /home/rikuho/.ros/log/2022-12-28-22-49-48-580537-LAPTOP-JHG3HSMU-838
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [840]
[INFO] [listener-2]: process started with pid [842]
[listener-2] [INFO] [1672235389.631230255] [listener]: Listen: 0
[listener-2] [INFO] [1672235390.105637283] [listener]: Listen: 1
[listener-2] [INFO] [1672235390.606707640] [listener]: Listen: 2
(Ctrl+cで終了)
```

## 貢献者
* [Ryuichi Ueda](https://github.com/ryuichiueda/my_slides/tree/master/robosys_2022)
このパッケージのコードは、本人の許可を得て自身の著作としたものです。

## ライセンス
* [BSD 3-Clause License](https://github.com/rikuhotakeda/mypkg/blob/master/RICENSE)

* @ 2022 Rikuho Takeda
