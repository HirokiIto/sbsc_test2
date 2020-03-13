* Notice
git push -u origin masterした時以下のエラーが出た時
remote: Permission to username/sbsc_test2.git denied to ***.
↓対処法
.git/configの中のurlにusername:passwordを加える(今回はgithubアカウントのもの)
[remote "origin"]
	url = https://username:password@github.com/username/sbsc_test2.git