### Notice
1. `git push -u origin master`して以下のエラーが出た時  
`remote: Permission to username/sbsc_test2.git denied to ***.`  
↓対処法
``` 
.git/configの中のurlにusername:password@を加える(今回はgithubアカウントのもの)  
 [remote "origin"]
	url = https://`username:password@`github.com/username/sbsc_test2.git
```

2. 特定のコミットまで戻したい時

``` 
$ git log //戻す対象のハッシュ値を調べる
commit ************************  
$ git reset --hard ハッシュ値
```

3. githubのブランチを強制的に書き換える
``` 
$ git push -f origin master 
```