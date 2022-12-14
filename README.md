# biblatex-jpa 日本心理学会風文献スタイル（2022年版）

これは、日本心理学会の「[執筆・投稿の手びき](https://psych.or.jp/manual/)」（2022年版）の書式にそった文献リストを作成するためのBibLaTeX用スタイルファイルです。日本語文献と外国語（英語）文献が混在する文献リストにも対応しています。

なお、このスタイルファイルは日本心理学会が配布するものではなく、作成者（芝田）が個人的に作成・管理しているものです。論文投稿等においてこのスタイルファイルで作成した文献リストが認められるかどうかについての保証はありませんので、その点についてはあらかじめご了承ください。

# 使用方法

## 導入
このスタイルを利用するには、biblatexフォルダにある3つのファイルを、タイプセットするファイルと同じディレクトリ、またはLaTeX管理下のフォルダに置いてください。

## jpa文献スタイルの指定
LaTeXやRMarkdownのファイルで、バックエンドを`Biber`に、文献スタイルを`jpa`に設定してください。LaTeXのプリアンブルにおける設定例は次のとおりです。RMarkdownでの指定方法については、RMarkdownのマニュアル等を参照してください。

```
\usepackage[backend=biber,style=jpa]{biblatex}
```

また、`\addbibresource{}`コマンドを使用して、使用する`bib`ファイルを指定してください。


## 文献ファイル（.bib）の作成
`jpa`スタイルはBibLaTeX形式の`.bib`ファイルを使用します。基本的にはBibTeX用の`.bib`ファイルと同じですが、全集の一部や翻訳書の処理のために、`related`フィールドなど、BibLaTeXで拡張されたフィールドを使用しています。文献ファイルにおける各文献項目の記載方法の詳細については、`doc/jpa-style.pdf`を参照してください。

## 文献の引用

本文中に文献を引用するには、`\textcite{}`コマンドを使用します（LaTeXの場合）。また、文献情報を括弧内に入れて示す場合には`\parencite{}`コマンドを使用します。`\textcite{}`コマンドで複数の文献を引用した場合，あるいは`\textcites{}`コマンドを使用した場合，文献と文献の間に「と」や「および」などの区切り文字が挿入されます。このとき，引用した文献の数が2つの場合には「山田（2020）と田中（2022）」，3つ以上の場合には「山田（2020），田中（2022），および佐藤（2021）」のように表示されます。

その他のコマンドについてはBibLaTeXのマニュアルを参照してください。

## 文献リストの作成

文献リストを表示したい箇所に、次の一文を入れることで引用文献リストが作成されます。

```
\printbibliography[title=引用文献]
```


# License

This work may be distributed and/or modified under the conditions of the LaTeX Project Public License, either version 1.3 of this license any later version. The latest version of this license is in http://www.latex-project.org/lppl.txt and version 1.3 or later is part of all distributions of LaTeX version 2005/12/01 or later.

This work consists of the files jpa.bbx, jpa.cbx, and jpa.dbx.

この著作物は、LaTeX Project Public License（バージョン1.3またはそれ以降）の条件下で配布・変更が可能です。このライセンスの最新版については[http://www.latex-project.org/lppl.txt](http://www.latex-project.org/lppl.txt)をご覧ください。

この著作物は、jpa.bbx、jpa.cbx、jpa.dbxの3つのファイルから構成されています。