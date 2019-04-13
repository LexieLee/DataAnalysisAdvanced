# DAP4: 创建一个 Tableau 故事

## Tableau Public 工作簿的链接

Tableau Public 工作簿的链接：[https://public.tableau.com/shared/NN9M234X4?:display_count=yes](https://public.tableau.com/shared/NN9M234X4?:display_count=yes)

```
～ 背景：泰坦尼克号上2224名乘客及船员的数据子集，包括了人口统计资料和乘客信息。点击查看更多信息[Titanic: Machine Learning from Disaster | Kaggle](https://www.kaggle.com/c/titanic )。
～ 目标：创建数据可视化，展现幸存者和遇难者的人口统计资料或乘客信息。
```
## 总结

> 不超过四句话，简要介绍你的数据可视化，并添加可帮助读者理解的上下文信息

泰坦尼克号遇难者人数过半，幸存者与性别、年龄、身份地位等有较大关系。性别：女性幸存率高于男性，年龄：小孩的幸存率高，其次是 30.5-40 岁的年轻人。身份地位：坐在头等舱的富人幸存率高，三等舱的人幸存率低。

从遇难者舱位图中，可以检索到每位遇难者的个人信息。

彩蛋：依据电影《泰坦尼克号》中的线索，在众多遇难者中找到了一位最像“Jack”的乘客——19 岁的小伙子 Soholt, Mr. Peter Andreas Lauritz Andersen。

## 设计

> 解释你所做的任何设计选择，包括收集反馈后对可视化进行的更改

故事分为五篇：

- 01 幸存者与性别的关系
	- 饼状图：幸存者和遇难者的整体比例
	- 饼状图：幸存者和遇难者的不同性别所占百分比
	- 背景图：泰坦尼克号
	- 筛选器：Sex
![](https://ws3.sinaimg.cn/large/006tKfTcly1g1jsd56nsrj30s00m0wqy.jpg)
- 02 幸存者与年龄的关系
	- 柱形图：幸存者和遇难者的不同年龄所占百分比（每 10 年划分一个年龄段）
	- 柱形图：不同年龄的幸存和遇难的比例
	- 散点图：不同年龄的幸存者和遇难者分布，不同形状代表舱位级别
	- 筛选器：Pclass、Survived
![](https://ws3.sinaimg.cn/large/006tKfTcly1g1jsd7l8bkj30q60mg77o.jpg)
- 03 幸存者与身份地位的关系
	- 条形柱状图：幸存者和遇难者在各舱位级别的分布
	- 堆叠柱状图：幸存率和舱位级别的关系
	- 箱线图：舱位级别和票价的关系
	- 筛选器：舱位级别（Pclass）、Survived，浮动的下拉菜单
	- 突出显示操作，运行操作方式为悬停
![](https://ws3.sinaimg.cn/large/006tKfTcly1g1jsdihrh8j30pb0mlabx.jpg)
- 04 怀念遇难者
	- 树状图：遇难者舱位图，舱位按照 `Cabin` 首字母划分
	- url 操作：从 Titanic 百科([Titanic Search Results for](https://www.encyclopedia-titanica.org/titanic-search.php?cx=partner-pub-8229361356428053%3A6873164966&cof=FORID%3A10&ie=UTF-8&q=))超链接每一位遇难者信息，运行操作方式为菜单
![](https://ws3.sinaimg.cn/large/006tKfTcly1g1jse4amwzj30s20mdagb.jpg)
- 05 彩蛋：寻找 Jack
	- 填充气泡图：遇难者名单
	- 筛选器：Survived、Sex、Sibsp、Parch、Age、Pclass、Cabin 等
	- 突出显示操作，仅针对 `Soholt, Mr. Peter Andreas Lauritz Andersen`，运行操作方式为悬停
![](https://ws3.sinaimg.cn/large/006tKfTcly1g1jseh8fypj30pt0mgmz9.jpg)

## 反馈

> 包含从第一份草图到最终可视化期间，你从他人那里获得的针对你的可视化的所有反馈

### 反馈 01

> 在“幸存者和身份地位关系”分析中，加入乘客在各舱位级别分布图，方便显示不同舱位级别的人数。

已增加该条形图

### 反馈 02

> 在“幸存者和性别关系“分析中，仅有两个图例，空白区域有点大，不够美观。

增加了一张图片，填充空白区域不足。

## 资源

> 列出你创建可视化时参考的任何来源

- [Save Workbooks to Tableau Public - Tableau](https://onlinehelp.tableau.com/current/pro/desktop/en-us/publish_workbooks_tableaupublic.htm)
- [Titanic: Machine Learning from Disaster | Kaggle](https://www.kaggle.com/c/titanic)
- [如何构建视图 URL - Tableau](https://onlinehelp.tableau.com/current/pro/desktop/zh-cn/embed_structure.htm)
- [Dashboard Interactivity Using Actions](https://www.tableau.com/learn/tutorials/on-demand/dashboard-interactivity-using-actions)

# CHANGELOG

- 190329 晴子创建 1.0