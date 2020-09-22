/*-----------------整理https://www.liaoxuefeng.com/wiki/896043488029600----------------*/
mkdir learngit                  // 创建版本库
cd learngit
pwd                             // 命令用于显示当前目录
git init                        // 命令把这个目录变成Git可以管理的仓库
git add readme.txt              // 命令git add告诉Git，把文件添加到仓;
								// 使用命令git add <file>，注意，可反复多次使用，添加多个文件
git commit -m 'add readme.txt'  // 命令git commit告诉Git，把文件提交到仓库;
								// -m后面输入的是本次提交的说明，可以输入任意内容
git status						// 命令随时掌握工作区的状态
git diff						// 命令可以查看修改内容
git log							// 命令显示从最近到最远的提交日志
git log --pretty=oneline		// 输出信息太多，可以加上--pretty=oneline参数
git reset --hard HEAD^			// 回退到上一个版本
git reflog						// 查看命令历史
git reset --hard commit_id		// 我们在版本的历史之间穿梭
								// commit_id版本ID
git checkout -- readme.txt		// 把readme.txt文件在工作区的修改全部撤销，用版本库里的版本替换工作区的版本
								// 让这个文件回到最近一次git commit或git add时的状态
git rm readme.txt				// 命令用于删除一个文件


/*------------------- 创建公匙SSH链接远程库 --------------------*/
1.	git bash输入	ssh-keygen -t rsa -C "youremail@example.com"	// 邮件地址换成你自己的邮件地址，然后一路回车使用默认值即可
																	// 成功后在用户主目录（C:\Users\YOURNAME\.ssh）里找到.ssh目录，里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥，可以放心地告诉任何人。
2.	登陆GitHub-->单击头像-->settings-->单击SSH and GPG keys-->New SSH key-->title随便填key填入id_rsa.pub所有内容-->Add Key
3.	单击头像旁的＋号-->单击New repository-->填写Repository name后直接创建-->跟着git remote提示一直在git上回车就OK


/*------------------- 创建分支 --------------------*/
git checkout -b dev				// git checkout命令加上-b参数表示创建并切换
								// 等价于git branch dev --> git checkout dev
git branch						// 命令查看当前分支;列出所有分支，当前分支前面会标一个*号。

dev分支的工作完成，我们就可以切换回master分支：
git checkout master				// 切换回master分支
git merge dev					// 命令用于合并指定分支到当前分支。

合并完成后：
git branch -d dev				// 删除dev分支

删除后，查看git branch，就只剩下master分支了。


