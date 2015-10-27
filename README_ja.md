---
jsPDF日本語対応化のメモ
---

# はじめに

このjsPDF_jaは、現在対応していない日本語のフォント出力を可能にするためのコードです。

当面は、完璧を目指すものではなく、業務上必要となる加工を行います。
日本語文字列を出力するには、特にaddFontなど本家のコードの内部を変更する必要があり、プラグインでの対応は困難かもしれませんので、
まずは、動作検証を含めて本家のコアなコードを加工する形で実装させて頂いております。

# APIドキュメント

jsPDFのAPIの用法についてのドキュメントは、特に日本語については不足していますので、APIのドキュメントを下に追記していきたいと思います。

## jsPDF APIリスト
| APIメソッド | 説明 |
--------|------
| [addPage](#addpage) | ページの追加 |
| [setPage](#setpage) | 作業対象のページの移動 |
| insertPage | ページの挿入 |
| movePage | ページの移動 |
| deletePage | ページの削除 |
| setDisplayMode | 表示モードの設定|
| text | 文字列の出力|
| lstext | 空白を入れる文字列の出力 |
| line | |
| clip | |
| lines | |
| rect | |
| triangle | | 
| roundRect | |
| ellipse | |
| circle | |
| setProperties | |
| setFontSize | |
| setFont | |
| setFontStyle | |
| getFontList | |
| addFont | |
| setLineWidth | |
| setDrawColor | |
| setFillColor | |
| setTextColor | |
| setLineCap | |
| setLineJoin | | 
| save | |

|APIプロパティ名 | 意味 |
| ------ | ----- |
| CapJoinStyles | |

## jsPDF プラグイン APIリスト


## 詳細APIドキュメント
### addPage

### setPage
#### 説明
作業対象のページへ移動する。
前提条件として既にページが作成されていなければならない。

#### 書式
setPage(_page_number_)

##### 引数
* _page_number_: 1から始まるページ番号。

#### サンプルコード
``` JavaScript

  doc.setPage(2);
  doc.text("This is page 2",100,30);

```

