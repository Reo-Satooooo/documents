# 阿部寛のホームページ風サイトを作成しよう
このドキュメントでは、阿部寛さんのホームページ風のサイトを作成するためのエッセンスと記事をまとめたものです。

## 阿部寛のホームページが優れている理由
俳優・阿部寛さんのホームページはトラディショナルなデザインですが、データ通信量を超過してしまい速度制限がかかってしまってもスムーズに表示ができるシンプルな構造です。  

[阿部 寛のホームページ](http://abehiroshi.la.coocan.jp/)

以下の記事では阿部寛さんのホームページが優れている理由を解説されています。

[なぜ阿部寛のホームページはベストを尽くさないのか。](https://qiita.com/mackey0022/items/0258ceddc7acd8626332)  


## 実際にホームページを作成してみる
以下の記事では作成方法が解説されています。SEOに関しても基本的な部分が解説されているので、一読することをオススメします。  

[阿部寛と学ぶHTMLチュートリアル](https://qiita.com/Michinosuke/items/ff696189ecd518da3d3a)  

ここからは上記のチュートリアル記事を補足する形で、解説をしていきます。Webページの作成において、基本的に使用するものは同じです。  

環境構築を完了し、HTMLファイルを作成した前提で解説します。

## まずはHTMLの雛形を入力する

まずはHTMLを記述する場合の基本の方を入力します。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```

VScodeで作成する場合 
```
html:5
```
で自動入力できます。

## 雛形に使用されているタグの解説

上記の雛形に使用されているタグについて解説します。  

既にHTMLについてある程度理解がある方や早くページを作成したい方は読み飛ばしていただいて結構です。

- Doctype宣言（ドクタイプ宣言）  
```html
<!DOCTYPE html>
```
Doctype宣言は、このページがどのバージョンのHTMLで記述されているかをしているものです。特に指定がない場合、HTML5を指します。

- html
```html
<html></html>
```
ページがHTMLで記述されていることを示します。Doctype宣言の直後に記述することが一般的です。開始タグと終了タグでワンセットです。

- head
```html
<head></head>
```
ページのタイトル、説明文、外部ファイル（CSSファイルなど）のリンク、ページ情報を記述します。ブラウザでは表示されません。

- meta
```html
<meta>
```
ページ情報、文字コード、説明文などを記述します。metaタグには終了タグがありません。

- title
```html
<title></title>
```
ページのタイトルを記述します。ブラウザのタブに表示されます。

- body
```html
<body></body>
```
ページのタイトル、説明文、外部ファイル（CSSファイルなど）のリンク、ページ情報を記述します。ブラウザでは表示されません。

## ページの中身を記述する
雛形ができたので中身を記述します。先ほどの雛形にコードを追加します。

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    <!--ここから-->
    <div>見出し１</div>
    <div>見出し２</div>
    <div>見出し３</div>
    <!--ここまで-->
</body>
</html>
```

コードを３行追加しました。ブラウザで表示してみましょう。  
```
見出し１
見出し２
見出し３
```
このようにbodyタグにテキストを記述するとページに表示ができます。

## 新たに出てきたタグの解説
- div
```html
<div></div>
```
このタグは単体で使用する場合、特に意味を持ちません。しかし、HTMLでページを作成する際に最も多様されるタグです。  

属性を付与することで意味付けを行い、テキストの配置やデザインを調整します。  

## divタグのみを用いてページをデザインする
チュートリアル記事のコードを引用させていただきます。
```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
  </head>
  <body>
    <div class="nav-wrapper">
      <div class="nav">
        <div class="nav-content"><div class="nav-icon"></div>トップ</div>
        <div class="nav-content"><div class="nav-icon"></div>経歴</div>
        <div class="nav-content"><div class="nav-icon"></div>趣味</div>
        <div class="nav-content"><div class="nav-icon"></div>作品</div>
        <div class="nav-content"><div class="nav-icon"></div>写真集</div>
        <div class="nav-content"><div class="nav-icon"></div>出版本</div>
        <div class="nav-content"><div class="nav-icon"></div>管理者</div>
      </div>
    </div>
    <div class="contents-wrapper">
      <div class="heading">阿部 寛のホームページ</div>
      <div class="contents-wrapper-inner">
        <div class="content-left">
          <div class="face-photo"></div>
          <div class="profile">
            阿部 寛（あべ ひろし）<br/>
            生年月日 1964年6月22日<br/>
            血液型 A型<br/>
            プロフィール
          </div>
          <div class="profile-english">
            If you have any enquiries regarding my TV drama or film, or would like to make an enquiry concerning future projects, please do not hesitate to contact me through the following email address.
          </div>
          <div class="mail">mail:shigeta@navy.plala.or.jp</div>
          <div class="profile-detail">
            所属:<br/>
            茂田オフィス<br/>
            107-0052<br/>
            東京都港区赤坂9-5-29<br/>
            赤坂ロイヤルマンション303<br/>
            TEL : +81-3-5410-8585<br/>
            FAX : +81-3-5410-0588<br/>
          </div>
        </div>
        <div class="content-right">
          <div class="news-heading">★★★　最新情報　★★★</div>
          <div class="news-list">
            <div class="news-list-content">
                <div class="news-list-title">・舞台</div>
                <div class="news-list-description">
                  彩の国シェイクスピア・シリーズ第35弾 『ヘンリー八世』 <br/>
                  2020年2月14日（金）～3月1日（日）
                </div>
            </div>
            <div class="news-list-content">
                <div class="news-list-title">・TV</div>
                <div class="news-list-description">
                    「まだ結婚できない男」<br/>
                    フジテレビ系連続ドラマ主演<br/>
                    毎週火曜日　21時～　放送中                   
                </div>
            </div>
            <div class="news-list-content">
                <div class="news-list-title">・映画</div>
                <div class="news-list-description">
                    「HOKUSAI」 <br/>
                    2020年・初夏 全国公開New!<br/>
                    <br/>
                      マレーシア映画「The Garden Of Evening Mists」<br/>
                    2020年公開予定
                </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </body>
</html>
```