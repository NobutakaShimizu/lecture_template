---
title: ホーム
layout: home
nav_order: 1
description: "講義トップ"
---

講義資料用のテンプレートです.
テンプレートの大元は[just-the-docs](https://github.com/just-the-docs/just-the-docs)です.
マークダウンで資料を記述できます. また数式はmathjaxで書けます.

# 数式の記述
例えば
```markdown
  グラフ$G=(V,E)$を考える.
```
というインラインに数式を含む文は

グラフ$G=(V,E)$を考える.

のように表示されます. 複数行にまたがる式変形などは
```text

$$
  \begin{align*}
    a &= b \\
      &= c
  \end{align*}
$$

```

と書けば

$$
  \begin{align*}
    a &= b \\
      &= c
  \end{align*}
$$

と表示されます (念の為, 最初と最後の`$$`の前後には一行空けておくと良いです.)

# 定理環境

定義などを述べるためのコールアウトは以下のように記述できます.

{: .definition }
> このボックスには**定義**を記します. 以下のように, 数式ボックスを内部に含めることができます:
>
>  $$
    \begin{align*}
      A_{u,v} = \begin{cases}
        1	& \text{if $\{u,v\} \in E$}, \\
        0 & \text{otherwise}.
      \end{cases}
    \end{align*}
>  $$
  
また, 以下のようにタイトルを自由に付与することができます.

{: .definition-title }
> 定義 (タイトル)
>
> 定義の例.

他にも命題,補題,定理,系のボックスが使えます.

{: .proposition }
> このボックスには**命題**を記します.

<details>
<summary style="display: list-item">証明</summary>

  このように, 折りたためる証明も書けます.
  内部でもインライン(例えば$a=b$)や独立した数式ブロックが書けます.
  $$
    \begin{align*}
      a &= b \\
        &= c.
    \end{align*}
  $$
  しかし, なぜかマークダウンはかけません.
  この中で強調表示したい場合は, 苦肉の策ですが, htmlタグを使って<b>装飾</b>しましょう.

  $\square$
</details>

{: .theorem }
> このボックスには定理(特に重要度の高い命題)を記します.

{: .lemma }
> このボックスには命題や定理を示すために必要な補助的な主張を記します

{: .corollary }
> このボックスには定理や命題などから直ちに成り立つ結果を記します.

{: .remark }
> このボックスには強調したい注釈が入ります.


## 新たなコールアウトの定義方法
他のボックス(例えば観察,未解決問題用のコールアウトなど)を自身で追加したいときは以下の二つのファイルを適切に編集してください.
- /_config.yml (コールアウトの宣言)
- /just-the-docs/_sass/support/_variables.scss (背景や文字の色の定義)