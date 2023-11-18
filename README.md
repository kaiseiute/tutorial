## チュートリアル
GitHubの練習をしよう！<br>
下記の手順にしたがって導入と練習をしよう！

## 用語一覧
| 用語 | 読み方 | 意味 |
| --- | --- | --- |
| Git || プログラムなどの変更履歴などを管理するバージョン管理システム |
| Github || Gitを分かりやすく扱うためのWebサービス |
| Repository| リポジトリ | ファイルやフォルダを保存するための場所 |
|| リモートリポジトリ | リモートのリポジトリ |
|| ローカルリポジトリ | ローカルのリポジトリ |
| Clone | クローン | 既存のリモートリポジトリをローカルリポジトリとして複製すること |
| Folk | フォーク | 既存のリモートリポジトリを自身のリモートポジトリとして複製すること |
| Branch | ブランチ | リポジトリの履歴を管理する機能 |
| Merge | マージ | フォークなどで分岐したリポジトリを統合すること |
| Commit | コミット | 変更をローカルリポジトリに適用すること |
| Commit Message | コミットメッセージ | コミットする際につけるメッセージ これがないとなにを変更したかわからなくなる |
| Push | プッシュ | ローカルリポジトリの変更をリモートリポジトリに適用すること |
| Pull | プル | リモートリポジトリの変更をローカルリポジトリに適用すること |
| Pull Request | プルリクエスト | ローカルリポジトリの変更をローカルリポジトリに適用するよう、管理者へ依頼すること |

## 手順
### ステップ1 Gitをインストールしよう
<details>
<summary>クリック</summary>

まずは大本であるGitをインストールしましょう<br>
[こちらから](https://git-scm.com/downloads)<br>
インストールができたら以下のコマンドを実行し、エラーが発生しなければ完了！
```
git --version
```
</details>

### ステップ2 Githubのアカウントを作ろう
<details>
<summary>クリック</summary>

Githubを使うにはアカウントが必要なので作成しましょう！<br>
[こちらから](https://github.com/join)
</details>

### ステップ3 "Hello World"と出力するプログラムのリポジトリを作ろう
<details>
<summary>クリック</summary>

- **リポジトリを作る**

  ![image](https://github.com/Fukupuro/tutorial/assets/123927296/9d683a49-2ad7-405d-a694-0c308b231483)
上の画像の**New**というところをクリックしてください
    ![image](https://github.com/Fukupuro/tutorial/assets/123927296/85dfd3f3-004e-4dad-b2c2-5932d738e357)
  #### Repository name 
  半角英数字記号で好きな名前をつけてください
  例. hello
  #### Description
  空白でOK
  <br>

  **Create repository**をクリック！
  ___
  ![image](https://github.com/Fukupuro/tutorial/assets/123927296/90900f8f-76fc-4f79-bc13-adc8b192252e)
この画面がでたら、画像下部分のhttps:/*という部分をコピーしてください<br>
これが作成したリポジトリのリポジトリパスです
  ___
- **自分のPCでの作業** <br>
  コマンドライン上でフォルダが作成されても構わない位置にcdコマンドなどで移動してください<br>
  移動出来たら以下のコマンドを実行してください
  ```
  git clone [リポジトリパス]
  ```
  そうすると、設定したリポジトリ名のフォルダができるので、そのフォルダをVScodeで開いてください
  ___

  ![image](https://github.com/Fukupuro/tutorial/assets/123927296/130c6d0e-7808-4c54-a9c3-ecf18f05f93e)<br>
  この画像でいうHELLOのすぐ右にある新しいファイルを作成ボタンをクリックし、ファイルを作ってください<br>
  ファイル名とプログラム言語はなんでも良いです 例. hello.js<br>
  次に、"Hello World"と出力させる簡単なプログラムを作成してください。一応サンプルを載せておきます
  - JavaScript(*.js)
    ```
    console.log("Hello World");
    ```
  - Python(*.py)
    ```
    print("Hello World")
    ```
  ___
  変更というところの右下にある＋マークをクリックしAddしてステージする
  ![image](https://github.com/Fukupuro/tutorial/assets/123927296/6d5919f6-382e-43e0-b311-aa05b6df6111)<br>
  
  メッセージ(コミットの上)に「 add [ ファイル名 ] 」と入力し、コミット
  ![image](https://github.com/Fukupuro/tutorial/assets/123927296/036fa27c-05a2-4553-9fb3-a17a06e63c29)
  
  ミートボールメニューから画像のように進んで、プッシュ
  ![image](https://github.com/Fukupuro/tutorial/assets/123927296/48fc2abb-e559-48b0-83c5-2e81623a32a0)

  すると…<br>
  ローカルリポジトリの変更がリモートリポジトリに適用されました！
  ![image](https://github.com/Fukupuro/tutorial/assets/123927296/b6d57380-eac3-4460-a585-055c8e5b1e66)

  以上で、"Hello World"と出力するプログラムのリポジトリを作ることができました！
</details>

### ステップ4 このリポジトリをフォークしてPullRequestを送ろう

<details>
<summary>クリック</summary>

もし仮に、複数人の開発者が関わるプロジェクトがあったとします。<br>そのプロジェクトで全員が好きなように開発を行い、それぞれが好きなようにリポジトリにプッシュしたとしたら...<br>
もちろん、同じファイルを複数人が別の実装を行う、そうです競合がおこってしまいます<br>
それを回避するためには、一度フォークしたり新たにブランチを作成したりして分岐させることが大切です<br>
分岐させれば、最終的にマージするタイミングで管理者が競合を解消することができます<br>
ここでは、リポジトリをフォークしてPullRequestを送ってみましょう！
___




</details>