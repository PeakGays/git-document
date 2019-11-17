## Git-Merge-Repositories

#### 场景
合并2个仓库  
1. 新系统作为一个模块并入  
2. svn转入git  
3. 新项目覆盖并入旧项目  

#### 步骤 
思想：将需要并入的仓库作为分支进行合并  

```shell script
git remote add ${PROJECT} ${PROJECT_URL}
git fetch ${PROJECT}
git merge ${PROJECT}/master --allow-unrelated-histories 
```

#### 注意 
第3条命令需要加入' --allow-unrelated-histories '是因为merge时，可能会遇到
'fatal: refusing to merge unrelated histories'，代表两个分支没有取得关系  

*第4条命令提交前需要解决冲突，冲突文件需要先提交



