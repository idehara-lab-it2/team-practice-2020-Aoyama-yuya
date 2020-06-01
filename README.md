# ユーザー２です

# チーム作業の準備（コンフリクト解決）

## GitHub におけるチーム作業（利点）

- 各自が**自分のブランチ**を持って同時並行で作業できる＝お互いに作業の邪魔にならない
- マージするのも簡単（特に問題がなければ）
- 必要であれば、他の人の成果を部分的にもらってくることもできる（今回の講義の範囲外）

## GitHub におけるチーム作業（難しいところ）

- 同じファイルを別々の人が同時に編集したら？　→　**コンフリクト**
- コンフリクトが起きたら、システム側では「どれが正しい文書か」を決められない
- その都度、人間が判断してやる必要がある
- A, B ２つのバージョンができてしまった場合の対応
  - A を正しいとして採用。B は採用しない
  - B を正しいとして採用。A は採用しない
  - A,B の両方をうまく組み合わせて正しいバージョンを作る
- これよりも複雑なコンフリクトの解決は今回の講義の範囲外

## github でのコンフリクトの解決手順

1. とりあえず、コンフリクトに構わずプルリクエストを作成する
1. 「コンフリクトがあるのでマージできない」と言われる
1. コンフリクトエディタを使って「最終的にこうしたい」という文書にする
1. コンフリクトが解決した（リゾルブした）と宣言する
1. プルリクエストをマージする

[公式ヘルプページ](https://help.github.com/ja/github/collaborating-with-issues-and-pull-requests/resolving-a-merge-conflict-on-github)

## 課題

自分でコンフリクトを起こし、それが解決しなさい。

### 課題の手順

1. `master` からブランチ `user1`, `user2` を作成する。（それぞれ別々の作業者という想定）
1. `user1` ブランチに切り替え、`idehara.md` を編集し、「専門：ＶＲ・ユーザインタフェース」と記述する。
1. `user2` ブランチに切り替え、`idehara.md` を編集し、「趣味：囲碁・将棋・ギャザ」と記述する。
1. `user1` ブランチから、`master` にプルリクエストを発行する。（これは問題なく成功する）
1. `user2` ブランチから、`master` にプルリクエストを発行する。（ここでコンフリクトが発生する）
1. コンフリクトを解消してマージし、専門と趣味が両方書き込まれた状態にする。

### 条件
- 作業に使ったブランチを削除しないこと（評価対象項目）
- 今回の課題について、`master` を直接編集しているコミットは評価の対象としない
- できる人が、ローカルリポジトリを利用して課題を作成することは禁止しないが、その場合でもリモートリポジトリに作業過程のブランチが残るよう配慮すること

（多摩大学経営情報学部　ＩＴ活用法２）
