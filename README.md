# NL2SQL
Natural Language to SQL( 以下简称`NL2SQL`)，是将自然语言（NL）转换成标准SQL语言的过程，属于自然语言处理-语义分析（Semantic Parsing）领域中的子任务。

它的目的可以简单概括为：**“打破人与结构化数据之间的壁垒”**，即用户可以通过文本描述完成对复杂数据库的查询工作，得到想要的结果。

## NL2SQL 简单示例

表_1-1

|  代码  |  名称  |    上市地点    | 收盘价 | 周涨跌幅 | 月涨跌幅 |
| :----: | :----: | :------------: | :----: | :------: | :------: |
| SINA.O |  新浪  |    纳斯达克    | 58.93  |  -4.52   |  8.791   |
| BITA.N |  易车  | 纽约证券交易所 | 18.11  |  -4.78   | -11.742  |
| JRJC.O | 金融界 |    纳斯达克    |  1.09  |  -9.17   |  2.834   |
| SFUN.N |  淘屏  |    纳斯达克    |  1.09  |  -9.17   |  2.834   |
| SFUN.N | 搜房网 | 纽约证券交易所 |  1.71  |  -9.52   |  28.575  |
| RENN.N | 人人网 | 纽约证券交易所 |  1.61  |  -9.55   |  14.18   |

Query：新浪和人人网的周涨跌幅分别是多少？

SQL：    **SELECT** 周涨跌幅 **FROM** 表_1-1  **WHERE** 名称=‘新浪’ **OR** 名称=‘人人网’

用户输入一句普通文本，模型将其转换为 SQL，查询数据库得到结果："-4.52, -9.55"

当然实际场景或业务中，需要查询的内容可能更加复杂。

## 已有数据集

现有NL2SQL数据集大致有以下几种

#### 1.WikiSQL

#### 2.Spider

#### 3.NL2SQL中文挑战赛数据集

```
数据集说明：
Todo
```

具体数据集可以在 ./data 目录下查看

## 解决方案

Todo



## 参考论文

#### `paper`下已有内容

```
1.《Editing-Based SQL Query Generation for Cross-Domain Context-Dependent Questions》
即 EditSQL 模型

2.《Towards Complex Text-to-SQL in Cross-Domain Database with Intermediate Representation》
即 IRNet 模型，Spider 数据集目前已经开源 SOTA 模型

3.持续更新中 ...
```

## 参考资料



