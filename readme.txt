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