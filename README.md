# Python-PDF2text

## 概要

pdf_PDF2textV.py は、pdf_PDF2text.py を縦書きのPDFファイル用に改良したものです。
２段組みの文書でも抽出できます。

## 使い方

```dosbatch
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


