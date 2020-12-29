# VSCodeの便利な拡張機能一覧

## プロジェクト管理機能

- Git Graph
    - ブランチとマージの関係が分かりやすい
    - コメントが時系列に表示されることに加えて、修正したプログラムも表示され、プログラムをクリックすると修正箇所に飛び、差分まで表示してくれる！！
- Git History
    - ブランチの作成や統廃合の作業が簡単にできる

## エディタ機能

- indent-rainbow
    - インデントに色がつき、何階層目かが分かりやすい
- Rainbow CSV
    - 列ごとに文字色を変えて表示してくれる。区切り文字はデフォルトでカンマやタブを認識するが、指定することもできる
    - 編集状態にはなってしまうが、列を揃えて表示してくれる機能もある
- Regrex Previewer
    - 正規表現を簡単にテストできるツール
- Trailing Spaces
    - 末尾の不要な空白をファイル保存時に自動的に削除してくれる

## Python

- Python Docstring Generator
    - docstringを"""+shiftまたはcmd+shift+2で生成
    - ユーザ定義のdocstringを使いたい場合は、下記設定を追加する

```
"autoDocstring.customTemplatePath": "/Users/kayo/GitHub/template-python/docstring.txt"
```

## その他
- SQLite
    - SQLiteデータベースを操作することができる。
    - *.sqlファイルにSQL文を記載して保存できログが残せる。
    - *.sqlファイルの選択したSQL文のみ実行することができるので、試行錯誤しながらクエリを決めることができる。不要になったクエリも残しておける。


