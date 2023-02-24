### 環境構築

```
$ make up
$ make install
```

## このリポジトリをコピーして新しいリポジトリを作成する場合
参考にしたサイト
https://blog.furu07yu.com/entry/github-clone-bare-repository

1. 複製先のリポジトリを作成する  
Githubの管理画面から複製先のリポジトリを事前に作成しておきます。

2. 複製元のベアリポジトリをクローンする
```
git clone --bare git@github.com:exampleuser/old_project.git
```

3. 新しいリポジトリをミラープッシュする
```
cd old_project.git
git push --mirror git@github.com:exampleuser/new_project.git
```
4. 複製元のベアリポジトリのディレクトリを削除する
```
cd ..
rm -rf old_project.git
```
5. 複製先のリポジトリをクローンする
```
git clone --bare git@github.com:exampleuser/new_project
cd new_project
```
