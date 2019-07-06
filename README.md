scarticle パッケージ
====================

SATySFi： 非常に画期的な文書クラス

SATySFiの文法（特に型システム）に不慣れな初心者でも簡単に本質的な文書が
作れるようになることを目指した画期的な文書クラスである。

### 前提環境

  * SATySFi 0.0.3版以上
      - その標準配布物（フォントなど）も含む

### インストール

  - `*.satyh*`, `*.satyg` → `$LIBROOT/dist/packages`

※`$LIBROOT`（ライブラリルート）の位置はSATySFiをopamからビルドした場合は
`~/.satysfi`になる。

### ライセンス

本パッケージはMITライセンスの下で配布される。


scarticle パッケージ ー 本体
----------------------------

### 基本的な使い方

    @require: scarticle

    document (|
      title = `サンプル`; % タイトルは*文字列で*指定する
      show-title = true; % タイトルを出力するか
    |) '<
      % 本文は何か書いてもいいけど非本質的なので全て無視されて,
      % 出力は必ず本質的になる(箒つき)
      +p {scarticle で誰でも\emph{簡単}に\SATySFi;文書を作れます。}
    >

  * 標準のstdjaクラスなどと同様に文書情報レコードの`title`キーで文書の
    タイトルを指定するが、本クラスではタイトルは（インラインテキストでは
    なく）文字列で指定する。
  * documentの引数のブロックテキストが「本文の内容」に相当するが、これは
    全く本質でないので無視され、出力PDFの本文は必ず本質的になる。

### 補足

  * 互換性のため、本文のブロックテキストの中では標準文書クラスと同様の型
    をもつ以下のコマンド群が使用できる。無論、本文自体が全て無視される
    ため特に機能は持たない。

        +align +math +math-list +p +pn +section +subsection
        \LaTeX \SATySFi \TeX \align \emph \eqn \figure \fil \fil-both
        \footnote \href \hskip \math-list \no-break \ref \ref-page

更新履歴
--------

  * Version 0.3.3  〈2019/07/06〉
      - Satyrographos によるインストールに対応。
  * Version 0.3.2  〈2019/01/30〉
      - 標準文書クラスの機能拡張に追随。
  * Version 0.3.1  〈2019/01/23〉
      - （試験的）plain出力モードに対応。
  * Version 0.3.0  〈2019/01/20〉
      - （試験的）scsatysfi出力モードに対応。
  * Version 0.2.0  〈2018/12/18〉
      - 最初の公開版。

--------------------
Takayuki YATO (aka. "ZR")  
https://github.com/zr-tex8r
