# 「Webシステム開発について」勉強会第10回 ハンズオン資料 の補足

栗原さんの利用した資料などを補足するサイトです



## 事前に必要な知識など

前回(9回)が終了しなかったので、資料には終わらなかったものが再掲されている



- [SPA (Single-page application)](https://developer.mozilla.org/ja/docs/Glossary/SPA)
- [AJAX (Asynchronous JavaScript And XML)](https://developer.mozilla.org/ja/docs/Glossary/AJAX)
- [ Bootstrap 3 系の公式ドキュメント ](https://getbootstrap.com/docs/3.4/getting-started/)
  - メニューに有る CSS, Components, JavaScript, Customize が全て。こんなことができるという点を把握しておけば、あとはページを見ればカスタマイズできる。



## 資料の補足（第9回と同じ内容記載）

### P6.ハンズオン 15 （第9回資料 : P28.ハンズオン 15 と同じ）


オンラインデモ

- [chapter02/04/sample1.html](https://ces-shiraishi.github.io/kurihara-training-part9/chapter02-04/sample1.html)
  - [codepen](https://codepen.io/ces-shiraishi/pen/YzWaGjK)


### P7.ハンズオン 16 （第9回資料 : P29.ハンズオン 16 と同じ）

オンラインデモ

- [chapter02/04/sample2.html](https://ces-shiraishi.github.io/kurihara-training-part9/chapter02-04/sample2.html)
  - [codepen](https://codepen.io/ces-shiraishi/pen/rNLdMKK)


### P8.ハンズオン 17 （第9回資料 : P30.ハンズオン 17 と同じ）

オンラインデモ

- [chapter02/04/sample4.html](https://ces-shiraishi.github.io/kurihara-training-part9/chapter02-04/sample4.html)
  - [codepen](https://codepen.io/ces-shiraishi/pen/WNxzGyj)


### P9.ハンズオン 18 （第9回資料 : P31.ハンズオン 18 と同じ）

ソースコードが同じ処理が記載してあったり、あまり良い内容ではなかったので、例として書くとしたら以下のようなコードになる。


```js
// アロー関数利用
var placeholder_action_on  = target => $(target).val("入力してください").css("color", "#CCC");
var placeholder_action_off = event  => $(event.currentTarget).val("").css("color", "#000");

$(function () {
    var input_element = $("input");

    placeholder_action_on(input_element);

    $("input")
        .one("focus", placeholder_action_off)
        .blur(function (event) {
            placeholder_action_on(event.currentTarget).one("focus", placeholder_action_off);
        });
});
```
オンラインデモ

- [chapter02/04/sample5.html](https://ces-shiraishi.github.io/kurihara-training-part9/chapter02-04/sample5.html)
  - [codepen](https://codepen.io/ces-shiraishi/pen/MWeVjGQ)


### P10.ハンズオン 19 （第9回資料 : P32.ハンズオン 19 と同じ）

オンラインデモ

- [chapter02/04/sample6.html](https://ces-shiraishi.github.io/kurihara-training-part9/chapter02-04/sample6.html)
  - [codepen](https://codepen.io/ces-shiraishi/pen/vYKRXjY)


### P12.ハンズオン 20 （第9回資料 : P34.ハンズオン 20 と同じ）

1. `$("span").css("font-weight")` の戻り値は数値を返すことがあり、 bold という文字列を返さないため、ハンズオンのソースは正しくない。
1. そもそも値がセットされていない場合は `undefined` を戻すので、それを利用する

オンラインデモ

- [chapter02/04/sample8.html](https://ces-shiraishi.github.io/kurihara-training-part9/chapter02-04/sample8.html)
  - [codepen](https://codepen.io/ces-shiraishi/pen/NWrYRYd)


### P13.ハンズオン 21 （第9回資料 : P35.ハンズオン 21 と同じ）

オンラインデモ

- [chapter02/04/sample9.html](https://ces-shiraishi.github.io/kurihara-training-part9/chapter02-04/sample9.html)
  - [codepen](https://codepen.io/ces-shiraishi/pen/YzWaGem)


### P14.ハンズオン 22 （第9回資料 : P36.ハンズオン 22 と同じ）

オンラインデモ

- [chapter02/04/sample10.html](https://ces-shiraishi.github.io/kurihara-training-part9/chapter02-04/sample10.html)
  - [codepen](https://codepen.io/ces-shiraishi/pen/dyXmMMY)



## 資料の補足（ここから第10回）


### P15.ハンズオン 1

職種的な問題で、アニメーションを実務で使うことはないが、以下のような命令は使うことがある。

- show
- hide
- toggle

オンラインデモ

- [chapter02/06/sample3.html](https://ces-shiraishi.github.io/kurihara-training-part10/chapter02-06/sample3.html)



### P15.ハンズオン 2

実務上はあまり利用しない

オンラインデモ

- [chapter02/06/sample10.html](https://ces-shiraishi.github.io/kurihara-training-part10/chapter02-06/sample10.html)



### P18.ハンズオン 3

実務上はあまり利用しないが、処理を理解するには良い教材と思う

オンラインデモ

- [chapter03/01/sample10.html](https://ces-shiraishi.github.io/kurihara-training-part10/chapter03-01/sample7.html)



### P18.ハンズオン 4


オンラインデモ

- [chapter03/02/sample10.html](https://ces-shiraishi.github.io/kurihara-training-part10/chapter03-02/sample2.html)



### P20.ハンズオン 05 (第4回資料 P07.ハンズオン 01と同じ)

第4回資料 P07.ハンズオン 01と同じ なので、それを掲載。
(chapter03/03/sample1.html)

オンラインデモ
- [chapter01/01/sample1.html](https://ces-shiraishi.github.io/kurihara-training-part9/chapter01-01/sample1.html)



### P23.ハンズオン 06

ajax で sample1.txt にリクエストを出して、その結果（レスポンス）を出しているという認識をすれば良いので、`sample1.txt` をブラウザでアクセスして見た結果を `<p>` 要素の中に入れていると思えばいい。

オンラインデモ
- [chapter02/05/sample1.html](https://ces-shiraishi.github.io/kurihara-training-part10/chapter02-05/sample1.html)
  - [chapter02/05/sample1.txt](https://ces-shiraishi.github.io/kurihara-training-part10/chapter02-05/sample1.txt)


※ load メソッドは[最新版では非推奨](https://api.jquery.com/category/deprecated/deprecated-1.8/)なので、利用しないこと


### P24.ハンズオン 07

考え方は同じ

オンラインデモ
- [chapter02/05/sample2.html](https://ces-shiraishi.github.io/kurihara-training-part10/chapter02-05/sample2.html)
  - [chapter02/05/sample2_load.html](https://ces-shiraishi.github.io/kurihara-training-part10/chapter02-05/sample2_load.html)


### P25.ハンズオン 07

恐らく誤記、表記されている内容は `P23.ハンズオン 06`


### P26.ハンズオン 08

成功以外に、失敗 (error) と 完了 (complete)も覚える必要があるが、そもそもこれらは1.8から[最新版では非推奨](https://api.jquery.com/category/deprecated/deprecated-1.8/)なので、利用しない事が多い。

- 成功
  - 1.8まで : success
  - 1.9から : done
- 失敗
  - 1.8まで : error
  - 1.9から : fail
- 完了
  - 1.8まで : complete
  - 1.9から : always


オンラインデモ
- [chapter02/05/sample3.html](https://ces-shiraishi.github.io/kurihara-training-part10/chapter02-05/sample3.html)
  - [chapter02/05/sample3.xml](https://ces-shiraishi.github.io/kurihara-training-part10/chapter02-05/sample3.xml)




### P28.ハンズオン 09

オンラインデモ
- [Bootstrap1.html](https://ces-shiraishi.github.io/kurihara-training-part10/Bootstrap1.html)



### P29.ハンズオン 10

オンラインデモ
- [Bootstrap2.html](https://ces-shiraishi.github.io/kurihara-training-part10/Bootstrap2.html)



### P30.ハンズオン 11

オンラインデモ
- [Bootstrap3.html](https://ces-shiraishi.github.io/kurihara-training-part10/Bootstrap3.html)




### P31.ハンズオン 12

オンラインデモ
- [Bootstrap4.html](https://ces-shiraishi.github.io/kurihara-training-part10/Bootstrap4.html)




### P33.ハンズオン 13

オンラインデモ
- [Bootstrap5.html](https://ces-shiraishi.github.io/kurihara-training-part10/Bootstrap5.html)



