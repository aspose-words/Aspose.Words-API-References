---
title: IMailMergeDataSourceRoot
second_title: Aspose.Words for Java API 参考
description: 实现此接口以允许来自自定义数据源的邮件与主从数据合并。
type: docs
weight: 651
url: /zh/java/com.aspose.words/imailmergedatasourceroot/
---
```
public interface IMailMergeDataSourceRoot
```

实现此接口以允许来自自定义数据源的邮件与主从数据合并。
## 方法

| 方法 | 描述 |
| --- | --- |
| [getDataSource(String tableName)](#getDataSource-java.lang.String-) | Aspose.Words 邮件合并引擎在遇到顶级邮件合并区域的开头时调用此方法。 |
### getDataSource(String tableName) {#getDataSource-java.lang.String-}
```
public abstract IMailMergeDataSource getDataSource(String tableName)
```


Aspose.Words 邮件合并引擎在遇到顶级邮件合并区域的开头时调用此方法。

当 Aspose.Words 邮件合并引擎用数据填充文档并遇到 MERGEFIELD TableStart:TableName 时，它调用[getDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasourceroot\#getDataSource-java.lang.String-)在这个对象上。您的实现需要返回一个新的数据源对象。 Aspose.Words 将使用返回的数据源来填充邮件合并区域。

如果具有指定名称的数据源（表）不存在，您的实现应返回 null 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tableName | java.lang.String | 模板文档中指定的邮件合并区域的名称。不区分大小写。 |

**退货：**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) - 将提供对指定表的数据记录的访问的数据源对象。