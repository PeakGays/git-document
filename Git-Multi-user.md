## Git-Multi-user

#### 场景
自己有个github，又有个gitlab，公司又来个私服gitlab


#### git config的优先级
local > global > system

示例：

```shell script
git config --local -l
```


####步骤 
1. 你需要生成对应的公钥和私钥，2个账户就生成2对
2. 将他们放入固定的位置,例如.ssh目录下
3. 关键点来了哦！！！你要记得在 ~/.ssh/config 中配置不同host不同的映射,下面是示例

```text
Host example                       # 关键词 
    HostName example.com           # 主机地址
    User root                      # 用户名
    # IdentityFile ~/.ssh/id_ecdsa # 认证文件
```


#### 注意
github根据邮箱和账户识别提交记录，请确保使用的config邮箱（user.email）对应github的邮箱
以及user.name对应github的账户名称