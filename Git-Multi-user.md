## Git-Multi-user

#### 场景
自己有个github，又有个gitlab，公司又来个私服gitlab


#### git config的优先级
local > global > system

示例：
`git config --local -l`


#### 注意
github根据邮箱和账户识别提交记录，请确保使用的config邮箱（user.email）对应github的邮箱
以及user.name对应github的账户名称