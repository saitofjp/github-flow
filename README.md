github-flow
===============

github-flowでサクサク

history
===
1. b1 branch init
2. b1 commit
3. b1 push orign b1:b1
4. b1 pull reqeust
  git bucket ui -> branches -> b1 compare -> create pull request
5. master merge pull request from b1
6. b2 branch init
7. b2 commit & push oring b2:b2

課題
==
* リモートのブランチの削除が追従に失敗する
pull requstのマージ時に、すぐにブランチ削除するとだめっぽい？

* ブランチ駆動は、マージするまで依存関係が
開発が重たくなりそう
