jscomplete-vim
==============

JavaScript の補完をする Vim plugin

omnifunc として使う
------------------

`omnifunc` に `jscomplete#CompleteJS` を設定すると動く。

    autocmd FileType javascript
      \ :setl omnifunc=jscomplete#CompleteJS

`.` や `[` 後のプロパティを補完します。

use as neocomplcache plugin
---------------------------

特に設定は必要ないです。(下記「拡張」はお好みで)

拡張
----

`autoload/js/` 以下に拡張用スクリプトがある

`g:jscomplete_use` または `b:jscomplete_use` にリストをいれると読み込まれる。

    :let g:jscomplete_use = ['dom', 'moz']
    " => autoload/js/dom.vim と autoload/js/moz.vim が読まれる

- `dom.vim` : DOM 系の補完リストを追加するよ
- `moz.vim` : Mozilla JavaScript の追加リスト
- `xpcom.vim` : Mozilla の XPCOM コンポーネント(`Components`オブジェクト) 系のリストを追加

