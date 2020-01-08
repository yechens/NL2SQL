# 2019NL2SQL挑战赛数据集

比赛说明：

首届中文NL2SQL挑战赛，使用金融以及通用领域的表格数据作为数据源，提供在此基础上标注的自然语言与SQL语句的匹配对，希望选手可以利用数据训练出可以准确转换自然语言到SQL的模型

Baseline 方案参考: https://github.com/ZhuiyiTechnology/nl2sql_baseline。

train.json文件中，每一行为一条数据样本。数据样例及字段说明例如下：

```
{
     "table_id": "a1b2c3d4", # 相应表格的id
     "question": "世茂茂悦府新盘容积率大于1，请问它的套均面积是多少？", # 自然语言问句
    "sql":{ # 真实SQL
        "sel": [7], # SQL选择的列 
        "agg": [0], # 选择的列相应的聚合函数, '0'代表无
        "cond_conn_op": 0, # 条件之间的关系
        "conds": [
            [1,2,"世茂茂悦府"], # 条件列, 条件类型, 条件值，col_1 == "世茂茂悦府"
            [6,0,1]
        ]
    }
}
```

其中，SQL的表达字典说明如下：

```
op_sql_dict = {0:">", 1:"<", 2:"==", 3:"!="}
agg_sql_dict = {0:"", 1:"AVG", 2:"MAX", 3:"MIN", 4:"COUNT", 5:"SUM"}
conn_sql_dict = {0:"", 1:"and", 2:"or"}
```

train.tables.json 文件中，每一行为一张表格数据。数据样例及字段说明例如下：

```
{
    "id":"a1b2c3d4", # 表格id
    "name":"Table_a1b2c3d4", # 表格名称
    "title":"表1：2019年新开工预测 ", # 表格标题
    "header":[ # 表格所包含的列名
        "300城市土地出让",
        "规划建筑面积(万㎡)",
        ……
    ],
    "types":[ # 表格列所相应的类型
        "text",
        "real",
        ……
    ],
    "rows":[ # 表格每一行所存储的值
        [
            "2009年7月-2010年6月",
            168212.4,
            ……
        ]
    ]
}
```

详细内容请参考：

https://tianchi.aliyun.com/competition/entrance/231716/information

