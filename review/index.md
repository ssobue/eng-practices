# コードレビューの開発ガイド

原文: https://github.com/google/eng-practices/blob/eaff1ef39cccbea085debf39809fc903c4786dab/review/index.md

## はじめに {#intro}

コードレビューとは、コードを修正した人以外がそのコードを確認・検証するプロセスをさします。
Googleでは、コードや製品の品質を保つためにコードレビューを行っています。
この開発ガイドでは、Googleのコードレビュー方法と基準を説明したものになります。
このページでは、コードレビュー方法の概要が記述されていて、他にも2つのドキュメントがあります。

-   **[コードレビューの方法](reviewer/index.md)**: コードレビューする人のための詳細なドキュメントです。
-   **[コード修正する人のガイド](developer/index.md)**: コード修正してレビューを受けるための詳細なドキュメントです。

## コードレビュアーは何を見ているのか？ {#look_for}

コードレビューでは以下の点を確認します。

-   **デザイン**: コードはしっかり設計され、対象のシステムに適切であるか？
-   **機能性**: コードは意図通りに動作するのか？ユーザーにとって必要なものか？
-   **複雑性**: コードはシンプルにできているか？ もし将来、他の開発者が見たときに理解してこれらを利用することができるのか？
-   **テスト**: コードに対する適切な自動テストが動作しているか？
-   **命名**: わかりやすい名前であるか？ (変数、クラス、メソッド など)
-   **コメント**: コメントはわかりやすく、意味のある内容であるか？
-   **スタイル・書式**: コーディング規約に則しているか？
-   **ドキュメント**: このコードに関連するドキュメントは更新しているか？

詳細は、 **[コードレビューの方法](reviewer/index.md)** を確認してください。

### ベストなレビューを選ぶ {#best_reviewers}

一般的には、期間内にレビュー対応をしてくれる人にお願いしたいものです。

最高のレビュアーとは、あなたが書いているコードに対して最も徹底的で正しいレビューをしてくれる人のことです。これは通常、コードの所有者を意味し、その所有者はOWNERSファイルに記載されている人である場合もあれば、そうでない場合もあります。場合によっては、異なる人にCLの異なる部分のレビューを依頼することもあります。

The best reviewer is the person who will be able to give you the most thorough
and correct review for the piece of code you are writing. This usually means the
owner(s) of the code, who may or may not be the people in the OWNERS file.
Sometimes this means asking different people to review different parts of the
CL.

理想的なレビュアーを見つけても、その人が利用できない場合は、少なくともその人に変更内容をCCで伝えるべきです。

If you find an ideal reviewer but they are not available, you should at least CC
them on your change.

### 対面式のレビュー {#in_person}

もし、あなたがコードの一部を、良いコードレビューをする資格のある人とペアプログラミングしたならば コードレビューを行う資格のある人とコードをペアプログラミングした場合、そのコードはレビューされたとみなされます。

対面式のコードレビューでは、レビュアーが質問し、変更を行った開発者がその場で話すこともできます。開発者が話しかけられたときだけ話すという方法もあります。

If you pair-programmed a piece of code with somebody who was qualified to do a
good code review on it, then that code is considered reviewed.

You can also do in-person code reviews where the reviewer asks questions and the
developer of the change speaks only when spoken to.

## 関連ドキュメント {#seealso}

-   [コードレビューの方法](reviewer/index.md): コードレビューする人のための詳細なドキュメントです。
-   [コード修正する人のガイド](developer/index.md): コード修正してレビューを受けるための詳細なドキュメントです。
