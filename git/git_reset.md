# git reset 

reset 默认参数为 --mixed

参数作用：
1. --mixed:回复到添加到索引之前的状态，即，回复到使用add添加之前的状态，git diff可查看 
2. --soft:回复到添加到索引之后，但是还没有提交到版本库的状态，git diff --cached 可查看
3. --hard:回复到work tree被修改之前的版本，即完全回复

>*git reset 回溯到git add之前的状态；git reset --soft回溯到git add之后的状态*

>*1和2都不会修改work tree 中的本地文件，只有3才会真正的改变本地文件，所以3存在一定风险*


	---------------|-----work tree-----|-------------index-----------|-----poresitory(HEAD)-----|
	                    ^                                    ^                                             ^
	                    |                                    |                                             |
	              --hard               --mixed(default)                     --soft