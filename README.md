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
8. あきた


課題
==
* リモートのブランチの削除が追従に失敗する
pull requstのマージ時に、すぐにブランチ削除するとだめっぽい？

* ブランチ駆動は、マージするまで依存関係が
開発が重たくなりそう



* ブランチ駆動は、マージするまで依存関係が
開発が重たくなりそう

* 変更を取り込む方法
　pullじゃなくて
　　どっちが良いんだろ
　	fetch-merge master
　  fetch-rebase master
　  

mege or rebase
===
masterの変更をトピックが取り込む方法はいくつかある
                                                         
マージ派
http://tech.oga-ria.com/manage-git-with-bitbucket-and-sourcetree/
＞rebaseは使わない
＞commitしたら即pushするので、リポジトリの不整合が発生する原因になりかねません。開発チーム内では使わないようにしています。

メリットとデメリットがあるよ
http://japan.blogs.atlassian.com/2013/11/git-team-workflows-merge-or-rebase/