# Python-PDF2text

## pdf_PDF2textVm

### 概要

pdf_PDF2textVm.py は、pdf_PDF2text.py を縦書きのPDFファイル用に改良したものです。

２段組みの文書から読んだ文字を上下別のテキストファイルに出力します。

### 使い方

```dosbatch
python pdf_PDF2textVm.py [-h] [-u s] [-d s] [-v n] [-f n] [-t n] [-s n] [-e n]
                        input_path

positional arguments:
  input_path        入力ファイル名

optional arguments:
  -h, --help          show this help message and exit
  -u s, --up s        上段用の出力ファイル名に付加する文字列(default:_u)
  -d s, --down s      下段用の出力ファイル名に付加する文字列(default:_d)
  -v n, --vertical n  段組みの切れ目 0の場合、用紙高さの半分(default:0)　
  -f n, --footer n    フッター位置(default:30)
  -t n, --top n       ヘッダー位置(default:1000)
  -s n, --s_page n    開始ページ(default:1)
  -e n, --e_page n    終了ページ(0:最終)(default:0)
```

## 概要 Description
PDFファイルを読んで文字をテキストファイルに出力します。
PDFファイル名が`新旧対照表.pdf`ならば、
上段は`新旧対照表_u.txt`、下段は`新旧対照表_d.txt`になります。
-u,-dオプションで、`_新`,`_旧`などの指定ができます。

## 特徴 Features

- ページのヘッダーやフッターを抽出の対象から除けます。  
	Exclude page headers and footers from extraction.  
- ページを指定して抽出できます。  
	You can specify the page to extract.  


## pdf_PDF2textV

### 概要

pdf_PDF2textV.py は、pdf_PDF2text.py を縦書きのPDFファイル用に改良したものです。

２段組みの文書でも抽出できます。

### 使い方

```dosbatch
python pdf_PDF2textV.py [-h] [-v n] [-f n] [-t n] [-s n] [-e n]
                        input_path [output_path]

positional arguments:
  input_path        入力ファイル名
  output_path       出力ファイル名(default:月日_時分_秒.txt)

optional arguments:
  -h, --help        show this help message and exit
  -v n, --vertical n  段組みの切れ目 0の場合、用紙高さの半分(default:0)　
  -f n, --footer n  フッター位置(default:30)
  -t n, --top n     ヘッダー位置(default:1000)
  -s n, --s_page n  開始ページ(default:1)
  -e n, --e_page n  終了ページ(0:最終)(default:0)
```

## 概要 Description
PDFファイルを読んで文字をテキストファイルに出力します。  
Read a PDF file and output characters to a text file.  

## 特徴 Features

- ページのヘッダーやフッターを抽出の対象から除けます。  
	Exclude page headers and footers from extraction.  
- ページを指定して抽出できます。  
	You can specify the page to extract.  
- 2段組みの文書でも抽出できます。  
	You can also extract even a two-tiered document.  

## 依存関係 Requirement

- Python 3.8.5
- pdfminer.six 20201018

## 使い方 Usage

```dosbatch
usage: pdf_PDF2text.exe [-h] [-b n] [-f n] [-t n] [-s n] [-e n]
                        input_path [output_path]

positional arguments:
  input_path        入力ファイル名
  output_path       出力ファイル名(default:月日_時分_秒.txt)

optional arguments:
  -h, --help        show this help message and exit
  -b n, --border n  段組みの切れ目 0の場合、用紙幅の半分(default:1)
  -f n, --footer n  フッター位置(default:30)
  -t n, --top n     ヘッダー位置(default:1000)
  -s n, --s_page n  開始ページ(default:1)
  -e n, --e_page n  終了ページ(0:最終)(default:0)
```

## インストール方法 Installation

- pip install pdfminer.six

## プログラムの説明サイト Program description site

[PDFからテキストを抽出(プログラム)【Python】 - プログラムでおかえしできるかな](https://juu7g.hatenablog.com/entry/Python/PDF/program)  

## 作者 Authors
juu7g

## ライセンス License
このソフトウェアは、MITライセンスのもとで公開されています。LICENSE.txtを確認してください。  
This software is released under the MIT License, see LICENSE.txt.


