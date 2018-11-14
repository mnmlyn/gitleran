# git log
git log -p 显示具体修改的内容
git log -stat 显示修改文件列表和统计信息
git log --shortstat 显示修改统计信息
git log --name-only 显示修改的文件名称
git log --name-status 显示修改的文件名称，以及M或A标识
git log --abbrev-commit 仅显示hash的前几位，而不是40位
git log --relative-date 时间使用相对时间
git log --graph 显示ASCII图在log左边
git log --pretty=oneline 显示为一行
git log --pretty=format:"%h %an /n%ad %ar %s" 格式化log输出
git log --oneline 显示为一行，且hash只显示前几位
git log -2 只显示最近的2条commit
git log --since="2018.04.30" 按照起始日期筛选commit
git log --until="2018.11.11" 按照截止日期筛选commit
git log --author="mnml" 按照作者筛选commit，可以部分匹配
git log --grep="rm" 按照commit message筛选commit
git log -S "hello" 按照文件中新添加或删除一个字符串，筛选commit
或者git log -S hello
为了顺便查看添加的内容可以加-p选项
git log -S hello -p 显示涉及到hello字符串增删的commit，显示修改
的内容
一个比较全面的git log命令如下:
git log --pretty=format:"%h %ar %s" --graph --since="2018.01.01" --author="mnmlyn"