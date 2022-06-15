---
marp: true
theme: uncover
class: invert
---

![bg left:20% 80%](https://kt3k.github.io/talk_deno_nikkei/assets/logo.svg)
### **Denoは混沌としたJS界を救う**

weblio study 開発チーム
鷹勇 @Takao

---

**今もなお、JavaScript界は、混沌に満ちています**

---

![bg left:40% 60%](https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Typescript_logo_2020.svg/1200px-Typescript_logo_2020.svg.png)
たしかに<span style="color:DodgerBlue ;">TypeScript</span>の普及により
JSによる開発は快適になりました。

---

![bg left:20% 50%](https://logos-download.com/wp-content/uploads/2018/05/Gulp_logo_red.png)
![bg 70%](https://uxwing.com/wp-content/themes/uxwing/download/10-brands-and-social-media/bower.png)
Gulp や bower は死に絶え、
公式のツール（npm）で開発ができるようになりました

---

![bg left:20% 90%](https://cdn.worldvectorlogo.com/logos/webpack.svg)
![bg 90%](https://images.ctfassets.net/in6v9lxmm5c8/4LlOrDdEXyxqi7wjIKAhgp/7bc2ba8009965c9fa02bf49493a13226/vite.svg)
webpack の席巻も
Vite が覆そうとしています。

---

![bg left:30% 70%](https://www.styled-components.com/atom.png)
ReactやVueのエコシステムは
CSSの名前衝突を現実的に解決しました

---

# しかし！
JS界には根本的な問題がある！！！！！

---

- node.js,npm,webpack などによる**複雑なビルド**をしないと**TSが使えない**
- npm による依存関係のブラックボックス化により、node_modules下は魔境と化している
- ESM? commonJS? 意味不明！（require, import/export 方式が混在する）
- npm による依存関係解決が複雑

---

しかし、これは node.js が急成長を遂げれた
一因になったとも考えます。
決して、無碍にはできない。

---

# <span style="color: green;">node.js</span> に変わるランタイム

---

![bg left:50% 100%](https://kt3k.github.io/talk_deno_nikkei/assets/logo.svg)
# **Deno**

---

# TypeScript
設定なしにTSを書ける！！！

---

# トップレベル await
async 関数の中でしか await は使えなかったが
トップレベルで await で書くことができる

---

# パッケージマネージャ is dead... 


```ts
export {
  add,
  multiply,
} from "https://x.nest.land/ramda@0.27.0/source/index.js";
```

---

# deno test
Jestをインストールしたりしなくていい！
```ts
import { assertEquals } from "https://deno.land/std@0.143.0/...";

// Compact form: name and function
Deno.test("hello world #1", () => {
  const x = 1 + 2;
  assertEquals(x, 3);
});

```

---

# require撤廃

---

# deno fmt, deno lint
ESLint? pritter?
必要ありません。

---

# deno bundle
フロントエンドの開発に使える

---

# 公式が盛ん
deno deploy などのサービスもある

---

# weblio studyでも一部導入中👍
---

今のJSに疲れたのであれば、Denoをオススメします！

---

**また、きっと、プログラミング（JS）を愛せるとおもいます**