# 二郎とTerminal Art

ラーメン二郎を食べた後、ふと42に戻って3時間くらいかけて作った謎の作品。

## 概要
このプロジェクトは、ターミナルを開いた際に自動で実行されるスクリプトを設定する方法を説明しています。この設定により、ターミナルを開くたびに指定されたアニメーションが再生されます。

# デモ

こんな感じ🎵

![2024-05-21_14 28 37](https://github.com/cimura/terminal_art/assets/144637453/e94857b6-2c34-4a02-a82a-031641ad0ecf)


ネズミが失踪した後にミ⚪︎キーマ⚪︎スの名言が見れます

## 手順

まずは何はともあれgit clone
```bash
git clone https://github.com/cimura/terminal_art.git
```
そしてそのディレクトリへ移動

```bash
cd terminal_art
```


### 1. スクリプトの準備
まず、ターミナルを開いた際に実行するスクリプトを用意します。例えば、animation.shという名前でスクリプトを作成します。スクリプトの内容は以下のようになります。



### 2. スクリプトの配置
作成したスクリプトをホームディレクトリのscriptsフォルダーに配置します。必要に応じてディレクトリを作成してください。また、そのファイルに実行権限を与えます。

```bash
mkdir -p ~/scripts
mv animation.sh ~/scripts/
chmod +x ~/scripts/animation.sh
```

3. .zshrcの編集
次に、ターミナルの設定ファイルである.zshrcを編集して、ターミナルが開かれたときにスクリプトが実行されるようにします。
今回はviで書き込むより手軽なのでechoを使いました。


```bash
echo 'if [ -f ~/scripts/animation.sh ]; then
    ~/scripts/animation.sh
fi' >> ~/.zshrc
```


4. 設定の反映
.zshrcを編集した後、変更を反映するためにターミナルを再起動するか、以下のコマンドを実行します。


```bash
source ~/.zshrc
```



5. 動作確認
ターミナルを再度開き、設定が正しく反映されているか確認します。スクリプトのアニメーションが実行されれば成功です。



# まとめ
この設定を行うことで、ターミナルを開くたびにカスタマイズされたアニメーションを楽しむことができます。一度試したらクセになるかもしれません。そう，ラーメン二郎のように


Enjoy making cute terminal art!!!

Thank you!
