# science_online_myselt
备份自己科学上网的相关配置


### 本地调用URL形式

http://127.0.0.1:25500/getprofile?name=%NAME%&token=%TOKEN%

- `%NAME%`：占位符，表示配置文件，默认是profiles目录下的文件

- `%TOKEN%`：占位符，表示自定义的密码，默认在`subconverter 解压目录下的 pref.toml 文件中`

eg:
`http://127.0.0.1:25500/getprofile?name=profiles/pref.ini&token=justdoit`

调用参数	必要性	  示例	解释
name	    必要	    profiles/formyairport.ini	指配置档案的存储位置(可使用基于pref 配置文件的相对位置)
token	     必要	     passwd	为了安全考虑必须设置token（详见 配置文件 中 [common] 部分 对 api_access_token 的描述）

### 参考官网
https://github.com/tindy2013/subconverter/blob/master/README-cn.md

### 本地调用需要注意的点（结合自己使用）
> 调用本地接口更新订阅时，如果发现自己添加的规则或者自己修改的项目在更新后并没有应用，并且未发现错误：
   清理本地路径下的 `cache`目录（），全部删除，默认优先应有本地的缓存，导致更新并没有立即触发应用，

> 自定义 `ruleset` 的时候，不要忘记**规则是按照从上往下顺序匹配到一个就应用的原则**。
