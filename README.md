github-flow
====

github-flowでサクサク

flow
===
1. init repo

2. clone
  git clone http://.../hoge.git
  ※以下、リモートリポジトリはorignと呼ぶ

3. push branch
  git branch {ブランチ名}
  git push orgin {ブランチ名}
  ※git push orgn {ローカルブランチ名}:{リモートブランチ名}でも良いけど合わせたほうが無難

4. commit&pus branch
  git commit しまくる！！
  git push orgin {ブランチ名}
  ※GitHub Flowでは、リモートブランチにもすぐさまpushして状況を共有する

5. pull reqeust
	web ui -> branches -> b1 compare to master -> create pull request

6. merge pull reqeust
	web ui -> pull reqeust -> 
	※ブランチの削除は任意で

7. merge from master
	他のブランチにマスターの変更を取り込もう
	やり方が二つあるため課題

s
課題
===

* リモートのブランチの削除が追従に失敗する
PullRequstのマージ後にすぐ削除すると、masterとブランチで差が付くため。
PullRequst語に、ブランチにmasterをマージすりゃ出来るが明らかにめんどい。

* ブランチ駆動にするとコンフリクトの検知がすごく後の方になる。
開発が重たくなりそう

* 変更を取り込む方法
orizin:master local:branchでpullでやるとだいだい壊れる
mergeかrebeaseになる
fetch-merge master
fetch-rebase master
　  

mege or rebase？
===
masterの変更をトピックが取り込む方法はいくつかある
                                                         
マージ派
http://tech.oga-ria.com/manage-git-with-bitbucket-and-sourcetree/
＞rebaseは使わない
＞commitしたら即pushするので、リポジトリの不整合が発生する原因になりかねません。開発チーム内では使わないようにしています。

メリットとデメリットがあるよ
http://japan.blogs.atlassian.com/2013/11/git-team-workflows-merge-or-rebase/


test history
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


