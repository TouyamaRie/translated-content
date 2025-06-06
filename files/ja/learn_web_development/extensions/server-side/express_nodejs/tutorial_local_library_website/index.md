---
title: "Express チュートリアル: 地域図書館のウェブサイト"
slug: Learn_web_development/Extensions/Server-side/Express_Nodejs/Tutorial_local_library_website
original_slug: Learn/Server-side/Express_Nodejs/Tutorial_local_library_website
---

{{LearnSidebar}}{{PreviousMenuNext("Learn/Server-side/Express_Nodejs/development_environment", "Learn/Server-side/Express_Nodejs/skeleton_website", "Learn/Server-side/Express_Nodejs")}}

実用的なチュートリアルシリーズの最初の記事では、これから学ぶことについて説明します。そして、私たちがこれから取り組んでいき、その後の記事で進化していく「地域図書館」のサンプルウェブサイトの概要を説明します。

| 前提条件: | [Express のイントロダクション](/ja/docs/Learn_web_development/Extensions/Server-side/Express_Nodejs/Introduction)を読んでください。以下の記事では、[Node 開発環境を設定する](/ja/docs/Learn_web_development/Extensions/Server-side/Express_Nodejs/development_environment)必要もあります。 |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| 目標:     | このチュートリアルで使用されているサンプルアプリケーションを紹介し、どのトピックがカバーされるのかを読者が理解できるようにします。                                                                                                                                                         |

## 概要

MDN "Local Library" Express (Node) チュートリアルへようこそ。このチュートリアルでは、地域図書館の目録を管理するために使用される可能性があるウェブサイトを開発します。

この一連のチュートリアル記事では、次のことを行います。

- Express Application Generator ツールを使用して、スケルトンウェブサイトとアプリケーションを作成します。
- Node ウェブサーバーを起動および停止します。
- データベースを使用してアプリケーションのデータを保存します。
- さまざまな情報を要求するためのルートを作成し、ブラウザーに表示するデータを HTML としてレンダリングするためのテンプレート ("ビュー" )を作成します
- フォームを操作します。
- アプリケーションを運用環境にデプロイします。

あなたはすでにこれらのトピックのいくつかについて学び、他のものについても簡単に触れました。チュートリアルシリーズの最後までに、簡単な Express アプリケーションを自分で開発するのに十分な知識があるはずです。

## LocalLibrary ウェブサイト

_LocalLibrary_ は、この一連のチュートリアルの過程で作成および進化するウェブサイトの名前です。ご想像のとおり、この ウェブサイトの目的は利用できる書籍を閲覧したり自分のアカウントを管理したりできる、地元の小さな図書館用のオンライン目録を提供することです。

この例は慎重に選択されています。必要なだけ詳細を表示することも、ほとんどすべての Express 機能を見せるために使用することもできるためです。さらに重要なことに、それはどんなウェブサイトでも必要とする機能性への*ガイド付きの*道筋を提供することができます：

- 最初のいくつかのチュートリアル記事では、図書館のメンバーがどの本が利用できるかを調べるために使用できる簡単な*ブラウズ専用*ライブラリーを定義します。これにより、ほぼすべての ウェブサイトに共通の操作、つまりデータベースからのコンテンツの読み取りと表示を探ることができます。
- 先へ進むにつれて、図書館の例は自然に拡張され、より高度な ウェブサイト機能を実演します。たとえば、新しい本を作成できるようにライブラリーを拡張し、これを使用してフォームの使用方法を示し、ユーザー認証をサポートすることができます。

これは非常に拡張可能な例ですが、_**Local**Library_ と呼ばれる理由があります。私たちは Express をすぐに使い始めるための最小限の情報を示すことを望んでいます。その結果、私たちは本に関する情報、本のコピー、作者、その他の重要な情報を保存します。ただし、図書館が貸し出す可能性のある他のアイテムに関する情報を保存したり、複数の図書館サイトやその他の "大きな図書館" 機能をサポートするために必要なインフラストラクチャを提供することはしません。

## 私は立ち往生しています、どこでソースを入手できますか？

チュートリアルを進めていくうちに、適切なコードスニペットを各ポイントにコピーして貼り付けることができます。また、他のコードも (ある程度の手引きを付けて) 自身で拡張することを望んでいます。

すべてのコードスニペットをコピーして貼り付けるのではなく、それらを入力してみてください。次回同様のコードを書くときに、コードに慣れ親しんでいることになるので、長期的に役に立ちます。

あなたが立ち往生したならば、[Github のここ](https://github.com/mdn/express-locallibrary-tutorial)で ウェブサイトの完全に開発されたバージョンを見つけることができます。

> [!NOTE]
> この文書でテストされた Node、Express、および他のモジュールの特定のバージョンは、プロジェクト [package.json](https://github.com/mdn/express-locallibrary-tutorial/blob/master/package.json) にリストされています。

## まとめ

_LocalLIbrary_ ウェブサイトと、これから学ぶことについて少し知りました。今度は私たちの例を含む[スケルトンプロジェクト](/ja/docs/Learn_web_development/Extensions/Server-side/Express_Nodejs/skeleton_website)の作成を開始します。

{{PreviousMenuNext("Learn/Server-side/Express_Nodejs/development_environment", "Learn/Server-side/Express_Nodejs/skeleton_website", "Learn/Server-side/Express_Nodejs")}}
