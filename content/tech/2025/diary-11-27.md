---
title: "Diary 11 27"
date: 2025-11-27T16:02:28+09:00
draft: false
tags: ["リポジトリあり"]
categories: []
showtoc: true
tocopen: false
---

## これはなに

オンライン会議中、何かガバを犯したとき青いオーラをまとうことにより "仕方ないね" と許されることを目的としたツール

### 前提

- 仮想カメラデバイス(OBS,Unity Capture)とか
- Python

### 使い方
```bash
python main.py
```

### 設定
```bash
python main.py --color 255,0,0 #デフォルト
python main.py --thickness 40
python main.py --blur 30
python main.py --camera 1 #複数あるときに
```

強さはリアルタイムで調節可能

### 使用例

UIを除いた映像がOBSのデバイスに流れます　会議でやらかしたとき、上のスライダーを0から増やすだけで親の加護が得られます

![使用例](/blog/images/tech/2025/11-27-a.png)

[リポジトリ](https://github.com/uraoz/GABA-Aura-Camera)