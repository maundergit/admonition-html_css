# admonition-html_css
HTMLで、注記／参照リストなどを、CSSとUnicode絵文字で見栄え良く作成したサンプル

## 概要

もともとは、[Markdown Preview Enhanced - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)で参照されている[Admonitions - Material for MkDocs](https://squidfunk.github.io/mkdocs-material/reference/admonitions/)をベースに、Unicode絵文字とCSS Animationで、注記や参照リスト専用のスタイル定義を作成してみたもの。

お硬い文書用ではなく、少しユニークな表現が許される文書用として作成

## 使い方

HTML文書のHEAD部で`admonitions.css` を呼び出して使用する。
```html
<link rel="stylesheet" href="admonitions.css>
```

HTMLのBODY部では、DIV要素のスタイル指定として使う。
以下のコードで`type`は、"abstract"などの種別、[icon[2,}]はオプションのアイコン種別の指定。
詳しくは`admonitions.html`のソース参照のこと。
```html
<div class="admonitions type">
	<div class="title [icon{2,}]">itle</div>
	<div>
		本文
	</div>
</div>
```

## 参照先

- [Markdown Preview Enhanced - Visual Studio Marketplace](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)
- [Admonitions - Material for MkDocs](https://squidfunk.github.io/mkdocs-material/reference/admonitions/)
- [Unicode - Compart](https://www.compart.com/en/unicode/)
- [Full Emoji List, v15.0](https://unicode.org/emoji/charts/full-emoji-list.html)
- [CSSだけでブルブル震わせる | q-Az](https://q-az.net/buruburu-hurueru-css/)
- [text-color-animation](https://codepen.io/alvarotrigo/pen/PoKMyNO)
- [Pure CSS text basic animations](https://codepen.io/alvarotrigo/pen/NWvQObB)


