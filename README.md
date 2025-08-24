## あいさつ

こんにちは、私は **Ryo** といいます。たまに Web 開発を行っている、そこらの者です。プログラミング言語は、TypeScript しか知りません。

私が Webアプリを開発するのに好んで使うのは、[**SvelteKit**](https://github.com/sveltejs/kit) です。

Web コンポーネントの支持者で、[**Lit**](https://github.com/lit/lit) を好みます。

JavaScript および TypeScript コミュニティを主に支援していて、最終的にこの世の中で使われるスクリプト言語は **TypeScript** になることを期待しています。

[Svelte](https://github.com/sveltejs/svelte)、[Web Awesome](https://github.com/shoelace-style/webawesome)、[TanStack](https://github.com/tanstack) の3つのプロジェクトは 将来 Web にとって必要不可欠となるでしょう！

## 開発したものたち

### Web サイト：

- [Kokomi's travel diary](https://kokomi-travel-diary.vercel.app/)

開発当時、AI の文章生成や画像生成が流行していたので、『それらを活かしてブログを作ってみたら面白いのではないだろうか』と思い立ち、そのときに SvelteKit でブログを作成するやり方を学んでいたので、その実践として開発してみました。画像生成で同じ雰囲気で、絵を描くことが思った以上に困難であると判明し、現在はあまり更新を行っていません・・・。

- [取手の美容室 Vell mo](https://vellmo.netlify.app/)

行きつけの美容室のウェブサイトを開発しました。初めの頃は、React Router を使用した React アプリとして開発していて、ルーターとしては、当時の自分は未熟で、コードの保守性のなさ、SEO対策のなさに不満を抱いていました。そこで、『様々な開発を経て得た、すべての反省を活かしたい！』として、デザインはほとんどそのままに、ゼロから1週間ほどで開発し直しました。

使い勝手が悪い面もありますが、Web標準であり、あらゆる場所で使えることがとっても魅力的です。

### コンポーネント：

**Lit** は私の最もお気に入りのライブラリであり、シンプルで強力な API が素晴らしいです。

- [Simplest](https://github.com/cat394/simplest)

  開発のきっかけとしては、マークダウンについて学習していた時に知った、 AST (Abstract Syntax Tree) という概念に興味を持ったことにありました。
  そこで私は独自の構文を AST に変換し CSS を生成できたら便利かもしれないなーと思い立って開発しました。
  基本的には、Web コンポーネントの属性に構文を記述することで、それを内部で AST から CSS に変換し、Shadow DOM に `<style>` タグを作成しその中に CSS を出力することで外部に漏れない限定的なスタイルを適用できるというものです。
  『スタイルを目的とした HTML 要素があるのだとしたら、どういった将来になっていたのだろう』を実現したものになります。Tailwind は `class` 属性で実現したものですが、これは HTML要素 で実現した、SVG のような発想になります。
  ただ私は結局のところ、CSS のセレクタの柔軟性に気づき、HTML と CSS は分離されているべきだという認識に至ったため、現在はパブリックアーカイブの状態にしました。

- [weather-widget](https://github.com/cat394/weather-widget)

  一日の天気を表示するためのコンポーネントです。友人から「学校から郵便番号を使った API を作成する課題がある」という話を聞き、「そのバックエンドの実装に、フロントエンドとして、お天気ウィジェットがあれば面白そうだ」と言ったことがきっかけで作りました。

### モジュール：

- **代表作: link-generator**

  [Link-generator](https://github.com/cat394/link-generator) は、TypeScript の文字列リテラル型の型推論を利用して、**完全に型安全に**パスを生成するモジュールを提供します。
  
  内部的に Map というデータ型を使用してリンクを効率的に生成し、フロントエンド/バックエンド問わず動作するため、SSR が主流な Web フレームワークでの開発に役立ちます。
  
  簡単なAPIと、便利なオプションを提供しています。たった一つの関数で準備 OK！画像のパスでもサイトのリンクでもなんでも型安全にできます！

### バックエンド：

- [Kokomi shopping server](https://github.com/cat394/kokomi-shopping-server)

  基本的なショッピングアプリの API サーバーです。Firebase Authentication によるユーザー認証、Firestore によるデータ保存、Stripe による決済処理、Cloudinary を使用した画像保存など、実際のサービスを利用したものになります。各エンドポイントのテストもしっかり行われており、RBAC による権限管理もテストされています。


