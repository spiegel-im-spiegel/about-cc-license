#クリエイティブ・コモンズ・ライセンスについて（PDF版）

このドキュメントは LuaLaTeX 用の文書ソースファイルです。
日本語のみの提供です。

## ドキュメントの情報

- Spiegel
- 2014-09-11

このドキュメントは Web 上で公開している「[クリエイティブ・コモンズ・ライセンスについて](http://www.baldanders.info/cc-license.shtml#aboutCC)」をベースに PDF 化したものです。
このドキュメントは cc-license の[「表示」ライセンス](http://creativecommons.org/licenses/by/4.0/)で提供しています。

## タイプセットについて

### TeX 環境とタイプセット手順

タイプセットに必要な TeX 環境については [TeX Live](http://www.tug.org/texlive/) 2014 以降が導入されていることを前提とします。

タイプセットは [LuaLaTeX](http://oku.edu.mie-u.ac.jp/~okumura/texwiki/?LuaTeX) を用い，ビルド作業には [latexmk](http://oku.edu.mie-u.ac.jp/~okumura/texwiki/?Latexmk) を用いています。
以下のコマンドで PDF まで自動でタイプセットを行います。

```
> latexmk about-cc-license.tex
```

なお，作者の環境は Windows 7 64bit です。リポジトリに挙がっている .latexmkrc の設定で上手く動かない場合は適宜修正して下さい。

- [LuaTeX-ja に関する覚え書き](http://www.baldanders.info/mdwiki/#!luatexja.md)

### 画像データについて

images ディレクトリ以下の Creative Commons 関連のライセンスマークやアイコンは「[データ・資料 - クリエイティブ・コモンズ・ジャパン](http://creativecommons.jp/about/downloads/)」のものを利用しています。
これらの画像データの取り扱いについては「[各種コンテンツの利用条件 - クリエイティブ・コモンズ・ジャパン](http://creativecommons.jp/policies/)」を参照して下さい。

なお， LaTeX 文書で利用するにあたり， PNG から PDF にフォーマット変換をしています。
フォーマット変換には [ImageMagick](http://www.imagemagick.org/) の convert コマンドを使用しました。

```
> convert by.png -colorspace CMYK EPDF:by.pdf
```

### タブレット用のレイアウト

文書ファイル中，プリアンブルに記述されている

```
%\setmainjfont[BoldFont=IPAexGothic]{KBMinchoM} % メインのフォントを KB明朝M に変更
%\usepackage[paperwidth=13.5cm, paperheight=17.25cm, top=0.5cm, left=0.5cm, right=0.5cm, bottom=0.5cm]{geometry} % Kindle layout
```

のコメント部分を解除することで Kindle 等のタブレットでの表示に適したレイアウトでタイプセットできます。

なお，メインのフォントには KB明朝M を指定しています。
KB明朝M は [Kobo Hack Uploader](http://ux.getuploader.com/KOBO_HACK/) で[取得](http://ux.getuploader.com/KOBO_HACK/search?q=KBMincho)することができます。
念のためバージョン0.43のファイルを[本家サイトに置いてあります](http://www.baldanders.info/fonts/KBMincho043.zip)。

KB明朝/KB明朝M フォントは [IPAex 明朝フォント](http://ipafont.ipa.go.jp/)の改変版で，画面の小さいタブレット等で見易いよう文字が太くなっています。

### PDF/A

この文書は PDF/A-1b 準拠の PDF として出力されています。
