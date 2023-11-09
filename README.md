# 大项目组写作更新
### 网址
1. http://anno-paper.rtfd.io
2. https://anno-paper.readthedocs.io/

## 协作更新方式
一篇文章一个jupyter notebook文件，另外加一个文章封面截图

1. 把238节点的`~/.ssh/id_rsa.pub`里的内容发给管理员
2. 在238节点找一个目录，然后执行`git clone git@github.com:annoroad/anno_papaer.git`
3. 编辑好jupyter notebook文件，请使用一个简短的有标识的命名，例如`scATACrice.ipynb`
4. 准备好一张png格式的截图作为这篇notebook文档的封面，png的命名最好和notebook的命名一致
5. notebook拷贝到对应的文件夹，例如`scATACrice.ipynb`要拷贝到scst文件夹
6. 文档封面`scATACrice.png`要拷贝到gallary-figs目录
7. 执行`git pull`命令，这一步是在推送前和远端仓库保持一致
8. 编辑对应类别的index.md，例如`scATACrice.ipynb`要编辑`scst/index.md`，把`scATACrice`加入文章索引
9. 编辑`gallary-fig.txt`，这是一个`tab`分隔的文件，记录的是封面图片和文档的对应关系
10. `git add -A`
11. `git commit -m "scATACrice"`
12. `git push`

> 每次添加新的**文档**从第5步骤开始即可。修改各分目录index.md、gallary-fig.txt以及all_papers.csv之前一定先执行`git pull`

## 更新注意事项
#### 1. 文档格式为`.ipynb`结尾的jupyter notebook格式
jupyter notebook里的每个cell支持`markdown`、`code`、`raw`三种格式，我们主要用到`markdown`和`raw`

其中`raw`主要用来添加文档的标签，便于网站的总体统计汇总

**jupyter notebook格式的好处是**

* 支持markdow格式
* 能够集成图片，不用另外构建图床
* notebook撰写时，在文档末尾加入一行`raw`格式的行来给文档添加标签，格式：`.. tags:: 2022, 植物三维基因组`，一般把年份和关联细类写上就行，如果网站中已经有类似标签，则建议重复使用，以便于统计。如果是一作或通讯的文章请添加标签：`一作或通讯`
* 文档的标签最好不要超过3个，不然网站看起来会很乱
* notebook添加图片很方便，截图粘贴到notebook一行中就行，注意事项是改一下名字，例如`![jxb_erac517-2.png](attachment:ac9c84-d04d46256.png)`，而不要用`![image.png](attachment:ac9c84-d04d46256.png)`，因为有重复**image.png**这样名字图的话图片显示会出现问题
