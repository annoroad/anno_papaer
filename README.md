# 大项目组写作更新
### 网址
1. http://anno-papaer.rtfd.io
2. https://anno-papaer.readthedocs.io/

## 协作更新方式
1. 申请账号
2. 联系管理员把自己的github账号加入https://github.com/annoroad/anno_papaer协作组

## 更新文件
一篇文章一个jupyter notebook文件，另外加一个文章封面截图

主要更新以下文件
1. 所属类别的index.md, 例如准备了一个叫abc.ipynb的文档放在了denovo目录下，那么denovo/index.md里就要加一行`./abc`
2. gallary-fig.txt, 此文件记录了notebook与文章封面截图对应关系，tab分隔
3. all_papers.csv

## 更新注意事项
#### 1. 文档格式为`.ipynb`结尾的jupyter notebook格式
jupyter notebook里的每个cell支持`markdown`、`code`、`raw`三种格式，我们主要用到`markdown`和`raw`

其中`raw`主要用来添加文档的标签，便于网站的总体统计汇总

**jupyter notebook格式的好处是**

* 支持markdow格式
* 能够集成图片，不用另外构建图床
* notebook撰写时，在文档末尾加入一行`raw`格式的行来给文档添加标签，格式：`.. tags:: 2022, 植物三维基因组`，一般把年份和关联细类写上就行，如果网站中已经有类似标签，则建议重复使用，以便于统计
* 文档的标签最好不要超过3个，不然网站看起来会很乱
* notebook添加图片很方便，截图粘贴到notebook一行中就行，注意事项是改一下名字，例如`![jxb_erac517-2.png](attachment:ac9c84-d04d46256.png)`，而不要用`![image.png](attachment:ac9c84-d04d46256.png)`，因为有重复**image.png**这样名字图的话图片显示会出现问题