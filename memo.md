やりたい
===============
* git-svnをweb stormで使いたいのだが？

flow
====

Git Flow
----
http://keijinsonyaban.blogspot.jp/2010/10/successful-git-branching-model.html
* いろいろ複雑

GitHub Flow
--
https://gist.github.com/Gab-km/3705015
* masterはリリース出来るもの。という考え
* ブランチを作って、Pull Requestでマージする


メモメモ
====

commit
----
* git commit -a で変更を自動でコミット

remoteとlocal
----
* remoteとlocalとoriginとmaster
  orignはremoteの名前。自由だけとoriginはルール

  git puhs orign master
  ==   git puhs orign master/master

* git remote
    git remote add remote-name url

forkとclone
----
* forkとclone
   cloneして、リクエストしたくなったらforkしてpush
   http://subtech.g.hatena.ne.jp/miyagawa/20090114/1231910461

fetchとpull
----
* fetch と pullの違い
  pull = fetch + merge

  http://qiita.com/y42sora/items/e082d64f3f8b424e9b7d
    ただし、mergeしたくない時にやってしまうと大変なことになる。
    そんな時は、戻したいコミットのIDを調べて、git reset --hard IDで元に戻せる。

upstream
----
* git pull を --set-upstream-to で引数無しで実行可能にする
  http://qiita.com/kjirou/items/e0469aac0e128be380d6
*  git push <repository> <refspec>
  -u オプションを付けると、対象のブランチをリモートリポジトリに追跡させることができます。 これによって、以降の push や fetch / pull コマンドで repository を省略した場合でも正しく変更内容を反映/取得することができるようになります。
  git push -u の -u は、 --set-upstream と同じで、追跡ブランチに登録するというオプション、だと思う。
* git config --global push.default upstream

mergeとrebase
----
* mergeとrebaseの違い
   rebaseは、ベースの再構築　ハッシュが変わるよー
   コミットに含む直前のコミットが変わるためpush後にrebaseするとpush出来ない


pull request
---
コミットをまとめる
* git merge --squash でブランチでの変更を1コミットにまとめてマージ
sourcetreeで追ってくれない。。。
* git rebase -i HEAD~~
packをsquashにする
他にも色々魔法がある


戻す
---
* git-revert
ある特定リビジョン（過去にcommitしたバージョン）に戻すパッチを自動生成してコミットする
* git-reset
ある特定リビジョン（ryに戻す（戻したリビジョン以降を無かったことにする）

pushされたものを完全に消すことはできない

コミット操作
----
* cherry-pick　抜き取る


その他
----
* sslがああ
git config --global http.sslVerify false

* GIT_SSHに環境変数を設定すると、GITはそれでSSHする、plink.exeを登録する

* Web Stormで、git push先を変える
git push ダイアログの「Push current branch to alternative branch」をチェックして、名前入れて
"更新"を押すと先が変わる
でも追従先がかわらん。。。

* Git 使い方 見出し一覧
http://transitive.info/article/git/

* 怖くないGit
rebaseとか丁寧。push後にrebaseするとpush出来ない理由とか/First Fowrad
http://www.slideshare.net/kotas/git-15276118