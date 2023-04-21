# typescript-training

Typescript を学習するためのリポジトリです

## このリポジトリでは何をするのか

Typescript の基本的な構文についてと、Typescript と Node を使った開発の流れを学びます。

Node.js を使う開発の流れを含んでしまいますが、基本的には **Typescript の学習に特化しています。**

### 最終的な目標

vue3 + typescript で TODO リストを作る
フロントエンドのフレームワークである`vue3`を使って、**TODO リスト**を作成します。

#### TODO リストに必要な機能

- やることを書き込むことができる
- やることを追加することができる
- やったことをチェックできる
- やったことを削除できる
- EX.何らかの方法でやることを保存することができる

これらの機能を実装するために最低限の Typescript の知識を身につけます。

## インストール + build

```bash
npm install

npm run dev
```

`clone`した後にリポジトリの**ルートディレクトリ**を開いて↑のコマンドを実行してください。
`npm run dev`で`Hello World`が出ればOKです

# Mission

## 最初に

今回の`Misson`では、`app.ts`を使って Typescript の基本的な構文を学びます。

**develop** ブランチから、自分の名前が付いたブランチを作成してください。

```
git branch feature/ichihara
```

**feature/${自分の名前}** というブランチを作成します。

---

## Mission 1 変数の型を定義してみよう

Typescript では、変数の型を定義することができます。

app.ts にある変数に型を定義してみましょう。
banana と名のついている変数は、型を定義していきましょう。

## Mission 2 関数の型を定義してみよう

Typescript では、関数の型を定義することができます。
ここでは、関数の引数と戻り値の型を定義してみましょう。

`bananaSell` という関数があります。
この関数の引数と戻り値の型を定義してみましょう。

_javascript では`function`を使って関数を定義しますが、Typescript では`function`を使わずに関数を定義することができます。_

```typescript
const exampleCallback = (arg: string): string => {
  return arg;
};
```

_のように、アロー関数を使って関数を定義することができます。_

## Misson 3 クラスの型を定義してみよう

Typescript では、クラスの型を定義することができます。
ここでは、クラスの型を定義してみましょう。

`app.ts`にある`Apple`というクラスの型を定義してみましょう。

- `name`というプロパティは`string`型
- `price`というプロパティは`number`型
- `mature`というプロパティは`"早" | "中" | "晩"`の型
- `getPrice`というメソッドは`number`型を返す
- `getMature`というメソッドは`string`型を返す
- EX.　これらの変数を使って、オリジナルの関数を作成してみましょう。

_以下のようにしてクラスを定義することができます。_

```typescript
class ExampleFluit {
  constructor(public name: string, public price: number, public mature: "早" | "中" | "晩") {
    this.name = name;
    this.price = price;
    this.mature = mature;
  }

  public getMature(): string {
    return this.mature;
  }

  public getPrice(count: number): number {
    console.log(${name}+"を"+${count}+"個買うと"+${this.price * count}+"円です。");
  }
}
```

## Mission 4 クラスをインスタンス化してみよう

Typescript では、クラスをインスタンス化することができます。
ここでは、クラスをインスタンス化してみましょう。

`app.ts`にある`Apple`というクラスをインスタンス化してみましょう。

名前は`王林`、値段は`100`、成熟度は`"晩"`でインスタンス化してみましょう。

## Mission 5 インターフェースを定義してみよう

Typescript では、インターフェースを定義することができます。
ここでは、インターフェースを定義してみましょう。

`app.ts`にある`Fluit`というインターフェースを定義してみましょう。

- `name`というプロパティは`string`型
- `origin`というプロパティは`string`型 (産地を表します)
- `price`というプロパティは`number`型

## Mission 6 インターフェースを拡張してみよう

Typescript では、インターフェースを拡張することができます。
ここでは、インターフェースを拡張してみましょう。(`type`とは異なり、拡張できます)

`app.ts`にある`Fluit`というインターフェースを拡張して`grape`というインターフェースを定義してみましょう。

- `isNeedSplint`というプロパティは`boolean`型
- `color`というプロパティは`"赤" | "白"`の型
- `size`というプロパティは`"小" | "中" | "大"`の型

## Misson 7-1 json を読み込んでみよう

Typescript では、json を読み込むことができます。
ここでは、json を読み込んでみましょう。

`./src/json/apple.json`を読み込んで、console に出力してみましょう。

## Misson 7-2 json を型付で読み込んでみよう

Typescript では、json を型付で読み込むことができます。
ここでは、json を型付で読み込んでみましょう。

`./src/json/apple.json`を型付で読み込んで、console に出力してみましょう。

参考になりそうな記事: [【TypeScript】外部の JSON ファイルを型付で読み込む](https://www.i-ryo.com/entry/2020/11/20/081558)

## Misson 8 これまでの流れを GitHub に上げてみよう

ここまでの作業の流れを`Github`で develop に`merge`するよう`Pull Request`を作成しましょう、コードレビューをしてもらいましょう。

基本的に時計回りで、コードを送りコードレビューをしてもらいましょう。
休んでいる人をレビュワーにはしないようにしましょう。

### Merge はしないでください。

## EX. ここまでの作業を行ってまだ時間が余ったら

今回の課題では、`Typescript`の基本的な構文を学びましたが、`Typescript`にはもっと多くの機能があります。
また、他の言語で学んだことを`Typescript`で使うこともできます。

for 文や if 文など、他の言語で学んだことを`Typescript`で使ってみましょう。
