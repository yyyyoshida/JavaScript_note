# DOM
## [DOMとは](https://pengi-n.co.jp/blog/js-dom/)
# 要素の取得
## [getElementById()](https://tech.mychma.com/javascript-getelementbyid/1506/)
## [getElementsByTagName()](https://tech.mychma.com/javascript-getelementsbytagname/1508/)
## [getElementsByClassName()](https://tech.mychma.com/javascript-getelementsbyclassname/1517/)
## [quearySelector()](https://wp-p.info/tpl_rep.php?cat=js-intermediate&fl=r4)
## [querySelectorALL()](https://wp-p.info/tpl_rep.php?cat=js-intermediate&fl=r4)
# 要素の操作    よく使うプロパティとメソッド
## テキストの変更
## [innerText](https://zenn.dev/rinasham/articles/e87999c2224d04)ページを含めて隠れている全部のテキストを取得
## [textContent](https://zenn.dev/rinasham/articles/e87999c2224d04)ページで見えているテキストのみ取得
## [innerHTML](https://zenn.dev/rinasham/articles/e87999c2224d04)要素の中身がHTMLを含めて取得
# 属性の変更
## [getAttribute()１](https://itsakura.com/js-getattribute#s2)
## [getAttribute()２](https://zenn.dev/ankouh/books/javascript-dom/viewer/b412c3)
## [setsAttribute()１](https://itsakura.com/js-getattribute#s2)
## [setsAttribute()２](https://zenn.dev/ankouh/books/javascript-dom/viewer/b412c3)
# スタイルの変更
## [.getComputedStyle()]()
## [style](https://www.cfxlog.com/javascript-dom/#rtoc-11)
## [クラスの操作](https://zenn.dev/ankouh/books/javascript-dom/viewer/b412c4)
## [classList.add()](https://www.cfxlog.com/javascript-dom/#rtoc-27)
## [classList.remove()](https://www.cfxlog.com/javascript-dom/#rtoc-27)
## [classList.contains()](https://www.cfxlog.com/javascript-dom/#rtoc-27)
## [classList.toggle()](https://www.cfxlog.com/javascript-dom/#rtoc-27)
*** 
# 親・子・兄弟要素
## 親要素
### [parentElement](https://web-tsuku.life/parentelement-get-parent/)
## 子要素
### [children](https://webstyle.work/javascript-children/)
## 兄弟要素
## 次の要素を返す
### [nextSibling](https://mebee.info/2021/01/11/post-27809/) nodeを返す。要素を返さない
### [nextElementSibling]() 要素を返す。nodeを返さない
## 手前の要素
### [previousSibling]() nodeを返す。要素を返さない
### [previousElementSibling]()要素を返す。nodeを返さない
***
# 要素を作る
## [createElement()](https://into-the-program.com/javascript-createelement/)
## 最後に追加
## [appendChild()](https://qiita.com/takuo_maeda/items/f531e7b5fe44c57242c3)
## [append()](https://tridentwebdesign.blog.fc2.com/e/append_etc)　文字列を直接渡せる
## 先頭に追加
## [prepend()](https://tridentwebdesign.blog.fc2.com/e/append_etc)
## 兄弟要素として追加
## [insertAdjacentElement()](https://developer.mozilla.org/ja/docs/Web/API/Element/insertAdjacentElement) 仮URL
## [after()](https://mebee.info/2021/01/15/post-27889/)
## [before()](https://mebee.info/2021/02/06/post-27881/)
## 要素を削除
## [remove()](https://developer.mozilla.org/ja/docs/Web/API/Element/remove)
# DOMイベント
## [clicks]()
## [マウスイベント](https://zenn.dev/mryhryki/articles/2022-10-06-mouse-events)
## [addEventListener()](https://qiita.com/mzmz__02/items/873118fbd8723c44956d)
## [addEventListenerのイベント](https://and-ha.com/coding/js-addeventlistener/)
## [第三引数](https://developer.mozilla.org/ja/docs/Web/API/EventTarget/addEventListener#options)
## [第三引数 例](https://tech.mychma.com/javascript-onceclick/1911/)
## [removeEventListener()](https://tech.mychma.com/javascript-removeeventlistener/1837/)
## thisを使って省略：thisの中は button と h1
## 省略前
```php
const makeRandomColor = () => {
  const r = Math.floor(Math.random() * 256);
  const g = Math.floor(Math.random() * 256);
  const b = Math.floor(Math.random() * 256);
  return `rgb(${r}, ${g}, ${b})`;
};

const buttons = document.querySelectorAll('button');
const h1s = document.querySelectorAll('h1');

for (let button of buttons) {
  button.addEventListener('click', function colorize() {
    button.style.backgroundColor = makeRandomColor();
    button.style.color = makeRandomColor();
  });
}
for (let h1 of h1s) {
  h1.addEventListener('click', function colorize() {
    h1.style.backgroundColor = makeRandomColor();
    h1.style.color = makeRandomColor();
  });
}
```
省略後
```php
const makeRandomColor = () => {
  const r = Math.floor(Math.random() * 256);
  const g = Math.floor(Math.random() * 256);
  const b = Math.floor(Math.random() * 256);
  return `rgb(${r}, ${g}, ${b})`;
};

const buttons = document.querySelectorAll('button');
const h1s = document.querySelectorAll('h1');

for (let button of buttons) {
  button.addEventListener('click', colorize);
}
for (let h1 of h1s) {
  h1.addEventListener('click', colorize);
}

function colorize() {
  this.style.backgroundColor = makeRandomColor();
  this.style.color = makeRandomColor();
}
```

# キーボードイベントとイベントオブジェクト
## [イベントオブジェクト](https://www.pyxofy.com/what-does-e-mean-in-javascript-function/)
## [キーボードイベント](https://qiita.com/nishimachikid/items/aca5b037af623e26929e)
## ページ全体に適応　window.addEventListener();
## [フォームイベント]()
## [preventDefault()](https://qiita.com/yokoto/items/27c56ebc4b818167ef9e)
## [elements]()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()
## []()

## []()
## []()
## []()
## []()
## []()

## []()
## []()

## []()

## []()


## []()


