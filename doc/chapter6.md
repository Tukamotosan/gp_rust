# 6. Modular, Grammatical and Developmental Tree-based GP

## Evolving Modular and Hierarchical Structures

### Automatically Defined Functions (AFS)

人間のプログラマは繰り返し使われる処理を関数やサブルーチンやクラスとしてコンポーネント化を行う. このような再利用は`車輪の再発明`を排除することができる. このコンポーネント化をうまく行うことでシステムを低レイヤから高レイヤに階層的に構築することができる. Kozaの考えた`Automatically Defined Functions (ADF)` はGPにこのような再利用可能なコンポーネントの様な物の進化を与えることが出来る. ここでは基本的なコンセプトを節目する. `ADF`の詳細は (Koza, 1994) で述べられている.

 ADFを用いると,プログラムは多様なコンポーネントを含むことが出来る. `result-producing branches (the RPB)`と同様に,これらは1つかそれ以上の`function-defining branches`を含むことが出来る. `RPB` は個体が評価された時に実行される `main` プログラである. しかし, `ADF`はお互いを実行することが出来る. 単一の`ADF`は同じ`RPB`から複数回実行されるか, `RPB`と他の`ADF`から実行される. 

 例えば,以下の個体は`RPB`と単一のADFからなる.

```math
RPB : ADF(ADF(ADF(x)))
```

```math
ADF : arg0 \times arg0
```

`$ADF$`は入力の2乗を計算する関数である. 上記の`$RPB$`は`$x^8$`を計算する.