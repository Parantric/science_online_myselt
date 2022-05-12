![](https://img.shields.io/badge/Clash%20for%20Window-V0.19.17-%234f8ef5) ![](https://img.shields.io/badge/By-Parantric-green)



![](https://raw.githubusercontent.com/Parantric/picture-bed/main/202205120701166.jpg)


# :bulb: Clash for Window 客户端使用记录

## :bookmark: 目录说明

### :file_folder:`OwnRuleSetList` ：存放 `clash for window` 的规则配置文件目录

### :page_facing_up: `subconverter_configs.ini` ：对应 `subconverter` 目录下 `config`目录下的 `.ini` 配置文件，为一些规则定义

### :page_facing_up: `subconverter_profiles.ini` ：对应 `subconverter` 目录下 `profile`目录下的 `.ini` 配置文件，作为 `clash` 调用参数的外部配置文件使用


## 📋本地调用URL形式

http://127.0.0.1:25500/getprofile?name=%NAME%&token=%TOKEN%

- `%NAME%`：占位符，表示配置文件，默认是profiles目录下的文件

- `%TOKEN%`：占位符，表示自定义的密码，默认在`subconverter 解压目录下的 pref.toml 文件中`
对应的参数项为：`api_access_token = "xxx"`，注意：双引号。

eg:
`http://127.0.0.1:25500/getprofile?name=profiles/pref.ini&token=justdoit`

调用参数	必要性	  示例	解释
name	    必要	    profiles/formyairport.ini	指配置档案的存储位置(可使用基于pref 配置文件的相对位置)
token	     必要	     passwd	为了安全考虑必须设置token（详见 配置文件 中 [common] 部分 对 api_access_token 的描述）

## 📌参考官网
https://github.com/tindy2013/subconverter/blob/master/README-cn.md

## ❗️本地调用需要注意的点（结合自己使用）
> 调用本地接口更新订阅时，如果发现自己添加的规则或者自己修改的项目在更新后并没有应用，并且未发现错误：
> 清理本地路径下的 `cache`目录（），全部删除，默认优先应有本地的缓存，导致更新并没有立即触发应用，

> 自定义 `ruleset` 的时候，不要忘记**规则是按照从上往下顺序匹配到一个就应用的原则**。



## :books:  关于 `github readme` 文件的书写格式，官方规范
https://docs.github.com/cn/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax
