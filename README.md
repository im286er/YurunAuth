# YurunAuth

基于YurunPHP框架的权限控制类，提供一个思路，如需在其它框架中使用请自行改造。

## 简介

### 表结构

role 是角色表，如：管理员

rule 是权限规则表，如：编辑用户权限

role_rule 是角色和权限规则的关联表

user_role 是用户和角色的关联表

user_rule 是用户和权限规则的关联表

### 思路

用户拥有角色的时候，就拥有这些角色下面所有的权限。

还可以为用户单独赋予这些角色所没有的权限。

判定用户是否拥有权限时，从角色拥有的权限 + 用户拥有的权限中进行查找。

## 安装

在您的composer.json中加入配置：

```json
{
    "require": {
        "yurunsoft/yurun-auth": "dev-master"
    }
}
```