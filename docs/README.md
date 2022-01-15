# 开发必看

## Git 使用规范

### 创建分支
```Shell
git checkout -b feature/id-description
```
### 删除分支
```Shell
git branch -D feature/id-description
```
### 切换分支
```Shell
git checkout feature/id-description
```
### 添加文件修改到暂存区
```Shell
# 暂存所有修改的文件
git add .

# 暂存某个文件
git add file_name
```
### 移动暂存区文件到本地仓库
```Shell
# 普通提交（参考分支命名）
git commit -m "feat: #id 描述"

# 解决冲突提交
git commit
```
### 推送当前分支到远程仓库
```Shell
# 当前分支第一次提交
git push --set-upstream origin feature/id-description

# 后面的提交
git push
```
### 暂存当前分支修改
```Shell
# 没有新增或删除的文件
git stash

# 存在新增或删除的文件
git stash save description -u
```
### 查看当前分支提交日志
```Shell
git log
```
### 拉取当前分支最新代码
```Shell
git pull
```

## Git 分支管理规范

### 分支命名
> 主分支：develop

> 功能分支：feature/id-description

> 修复分支：bugfix/id-description

*id： TAPD 对应工单编号，一般以 10XXXXX 开头*

*description: 创建分支的意图说明，使用英文描述*


### 创建分支
所有分支必须从develop分支切出

### 合并分支
所有分支必须合并到develop分支

## TAPD 使用规范
- 使用企业微信登录TAPD
- 创建需求或者缺陷
- 添加描述、严重程度、紧急程度、处理人、关联模块等信息

## 代码仓库维护规范
- TAPD领取任务
- 创建分支（遵守上述“分支命名”规范）
- 编码
- 提交代码
- 在对应仓库添加merge request，增加指派人，复制TAPC工单url到和并请求的描述中
- 点击创建，将文件tab页的url复制到工单的描述中，格式为：merge request: URL