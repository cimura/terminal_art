# 二郎とTerminal Art

ラーメン二郎を食べた後、ふと42に戻って3時間くらいかけて作った謎の作品。

## 概要
このプロジェクトは、ターミナルを開いた際に自動で実行されるスクリプトを設定する方法を説明しています。この設定により、ターミナルを開くたびに指定されたアニメーションが再生されます。

## 手順
1. スクリプトの準備
まず、ターミナルを開いた際に実行するスクリプトを用意します。例えば、animation.shという名前でスクリプトを作成します。スクリプトの内容は以下のようになります。

sh
コードをコピーする
#!/bin/bash

# アニメーションの実行内容
echo "Welcome to your customized terminal!"
# ここにアニメーションの内容を書きます
2. スクリプトの配置
作成したスクリプトをホームディレクトリのscriptsフォルダーに配置します。必要に応じてディレクトリを作成してください。

sh
コードをコピーする
'''python
mkdir -p ~/scripts
mv animation.sh ~/scripts/
'''
3. .zshrcの編集
次に、ターミナルの設定ファイルである.zshrcを編集して、ターミナルが開かれたときにスクリプトが実行されるようにします。

sh
コードをコピーする
vi ~/.zshrc
以下の内容を.zshrcの最後に追加します。

sh
コードをコピーする
if [ -f ~/scripts/animation.sh ]; then
    ~/scripts/animation.sh
fi
このコードは、~/scripts/animation.shファイルが存在する場合にそのスクリプトを実行することを意味します。

4. 設定の反映
.zshrcを編集した後、変更を反映するためにターミナルを再起動するか、以下のコマンドを実行します。

sh
コードをコピーする
source ~/.zshrc
5. 動作確認
ターミナルを再度開き、設定が正しく反映されているか確認します。スクリプトのアニメーションが実行されれば成功です。

まとめ
この設定を行うことで、ターミナルを開くたびにカスタマイズされたアニメーションを楽しむことができます。ラーメン二郎のように、一度試したらクセになるかもしれません。




# 二郎とTerminal Art

ラーメン二郎を食べた後、ふと42に戻って3時間くらいかけて作った謎の作品。

# DEMO

こんな感じ🎵

![](https://cpp-learning.com/wp-content/uploads/2019/05/pyxel-190505-161951.gif)

This animation is a "Cat playing on trampoline"!
You can get basic skills for making physics simulations.

# Features

Physics_Sim_Py used [pyxel](https://github.com/kitao/pyxel) only.

```python
import pyxel
```
[Pyxel](https://github.com/kitao/pyxel) is a retro game engine for Python.
You can feel free to enjoy making pixel art style physics simulations.

# Requirement

* Python 3.6.5
* pyxel 1.0.2

Environments under [Anaconda for Windows](https://www.anaconda.com/distribution/) is tested.

```bash
conda create -n pyxel pip python=3.6 Anaconda
activate pyxel
```

# Installation

Install Pyxel with pip command.

```bash
pip install pyxel
```

# Usage

Please create python code named "demo.py".
And copy &amp; paste [Day4 tutorial code](https://cpp-learning.com/pyxel_physical_sim4/).

Run "demo.py"

```bash
python demo.py
```

# Note

I don't test environments under Linux and Mac.

# Author

* Hayabusa
* R&D Center
* Twitter : https://twitter.com/Cpp_Learning

# License

"Physics_Sim_Py" is under [MIT license](https://en.wikipedia.org/wiki/MIT_License).

Enjoy making cute physics simulations!

Thank you!
