# admonition-html_css

HTMLとCSSで、注記／参照リストなどをCSSとUnicode絵文字で見栄え良く作成したサンプル

## 概要

もともとは、[Markdown Preview Enhanced - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)で参照されている[Admonitions - Material for MkDocs](https://squidfunk.github.io/mkdocs-material/reference/admonitions/)をベースに、Unicode絵文字とCSS Animationだけで、注記や参照リスト専用のスタイル定義を作成してみたもの。

お硬い文書用ではなく、少しユニークな表現が許される文書用として作成
合わせて、使えそうなUnicode絵文字もリストアップ。

表示環境によりUnicode絵文字が異なるため、環境によっては意図とは異なる結果になるかもしれない

確認／調整はMS-Windows 10上で実施。
iPadOS上では、今のところあまり良い表示なっていない(多分。font-familyの指定の問題)。

### 定義されたスタイル項目

以下の大雑把な分類に対してスタイルを定義

<ul style="column-count:2;list-style-type: '■ ';">
    <li>Abstract(概要)</li>
    <li>Note(ノート、コメント)</li>
    <li>Hint(ヒント)</li>
    <li>Example(例)</li>
    <li>Thinking(考察／検討課題)</li>
    <li>Refrence(参照／参考項目)</li>
    <li>Information(参考／補足情報)</li>
    <li>Important(重要項目)</li>
    <li>Alert/Caution/Warning/Attention(注意／警告項目)</li>
    <li>Error(エラー／間違い)</li>
    <li>Fatal(致命的なエラー／間違い)</li>
    <li>Question and Answer(質問と回答)</li>
    <li>Topic(トピック)</li>
    <li>Quote(引用参照)</li>
    <li>Secret(秘密事項)</li>
</ul>

## 使い方

HTML文書のHEAD部で`admonitions.css` を呼び出して使用する。

```html
<link rel="stylesheet" href="admonitions.css">
```

HTMLのBODY部では、DIV要素のスタイル指定として使う。
以下のコードで`type`は、"abstract"などの種別、[icon[2,}]はオプションのアイコン種別の指定。
詳しくは`admonitions.html`のソース参照のこと。

```html
<div class="admonitions type">
	<div class="title [icon{2,}]">title</div>
	<div>
		本文
	</div>
</div>
```

## 使用例

<link rel="stylesheet" href="https://maundergit.github.io/admonition-html_css/admonitions.css">

以下にいくつかの例は以下の通り、使用例全体は[デモページ](https://maundergit.github.io/admonition-html_css/admonitions.html)を参照のこと


```html
<div class="admonitions note">
    <div class="title"> Note title</div>
    <div>
        本文
    </div>
</div>
```
<div class="admonitions note">
    <div class="title"> Note title</div>
    <div>
        本文
    </div>
</div>

```html
<div class="admonitions example">
	<div class="title">Example title</div>
	<div>
		本文
		<pre>
1st
2nd
Sample</pre>
	</div>
</div>
```
<div class="admonitions example">
	<div class="title">Example title</div>
	<div>
		本文
		<pre>
1st
2nd
Sample</pre>
	</div>
</div>

```html
<div class="admonitions thinking">
	<div class="title icon4"> thinking title</div>
	<div>
		本文
	</div>
</div>
```
<div class="admonitions thinking">
	<div class="title icon4"> thinking title</div>
	<div>
		本文
	</div>
</div>

```html
<div class="admonitions warning">
	<div class="title icon2">warning title</div>
	<div>
		本文
	</div>
</div>
```
<div class="admonitions warning">
	<div class="title icon2">warning title</div>
	<div>
		本文
	</div>
</div>

```html
<div class="admonitions error">
	<div class="title icon2">error title</div>
	<div>
		本文
	</div>
</div
```
<div class="admonitions error">
	<div class="title icon2">error title</div>
	<div>
		本文
	</div>
</div

```html
<div class="admonitions fatal">
	<div class="title icon4">fatal title</div>
	<div>
		本文
	</div>
</div
```
<div class="admonitions fatal">
	<div class="title icon4">fatal title</div>
	<div>
		本文
	</div>
</div

```html
<div class="admonitions quote">
	<div class="title">quote title</div>
	<div>
		本文
		<blockquote>
		参照した部分
		</blockquote>
	</div>
</div>
```
<div class="admonitions quote">
	<div class="title">quote title</div>
	<div>
		本文
		<blockquote>
		参照した部分
        </blockquote>
	</div>
</div>

```html
<div class="admonitions secret">
	<div class="title icon8">Secret title</div>
	<div>
		本文
	</div>
</div>
```
<div class="admonitions secret">
	<div class="title icon8">Secret title</div>
	<div>
		本文
	</div>
</div>

## 参照先

- [Markdown Preview Enhanced - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)
- [Admonitions - Material for MkDocs](https://squidfunk.github.io/mkdocs-material/reference/admonitions/)
- [Unicode - Compart](https://www.compart.com/en/unicode/)
- [Full Emoji List, v15.0](https://unicode.org/emoji/charts/full-emoji-list.html)
- [CSSだけでブルブル震わせる | q-Az](https://q-az.net/buruburu-hurueru-css/)
- [text-color-animation](https://codepen.io/alvarotrigo/pen/PoKMyNO)
- [Pure CSS text basic animations](https://codepen.io/alvarotrigo/pen/NWvQObB)

