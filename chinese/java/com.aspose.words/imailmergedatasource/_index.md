---
title: IMailMergeDataSource
second_title: Aspose.Words for Java API 参考
description: 实现此接口以允许来自自定义数据源（例如对象列表）的邮件合并。
type: docs
weight: 650
url: /zh/java/com.aspose.words/imailmergedatasource/
---
```
public interface IMailMergeDataSource
```

实现此接口以允许来自自定义数据源（例如对象列表）的邮件合并。还支持主从数据。

创建数据源时，应将其初始化为指向 BOF（在第一条记录之前）。 Aspose.Words 邮件合并引擎将调用[moveNext()](../../com.aspose.words/imailmergedatasource\#moveNext--)前进到下一条记录，然后调用**M:Aspose.Words.MailMerging.IMailMergeDataSource.GetValue(System.String,System.Object@)**对于它在文档或当前邮件合并区域中遇到的每个合并字段。
## 方法

| 方法 | 描述 |
| --- | --- |
| [getChildDataSource(String tableName)](#getChildDataSource-java.lang.String-) | Aspose.Words 邮件合并引擎在遇到嵌套邮件合并区域的开头时调用此方法。 |
| [getTableName()](#getTableName--) | 返回数据源的名称。 |
| [getValue(String fieldName, Ref fieldValue)](#getValue-java.lang.String-com.aspose.words.ref.Ref-) |  |
| [moveNext()](#moveNext--) | 前进到数据源中的下一条记录。 |
### getChildDataSource(String tableName) {#getChildDataSource-java.lang.String-}
```
public abstract IMailMergeDataSource getChildDataSource(String tableName)
```


Aspose.Words 邮件合并引擎在遇到嵌套邮件合并区域的开头时调用此方法。

当 Aspose.Words 邮件合并引擎用数据填充邮件合并区域并遇到 MERGEFIELD TableStart:TableName 形式的嵌套邮件合并区域的开头时，它调用[getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource\#getChildDataSource-java.lang.String-)在当前数据源对象上。您的实现需要返回一个新的数据源对象，该对象将提供对当前父记录的子记录的访问。 Aspose.Words 将使用返回的数据源来填充嵌套的邮件合并区域。

以下是实施的规则[getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource\#getChildDataSource-java.lang.String-)必须遵循。

如果此数据源对象表示的表具有指定名称的相关子（详细信息）表，则您的实现需要返回一个新的[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource)将提供对当前记录的子记录的访问的对象。这方面的一个例子是 Orders / OrderDetails 关系。让我们假设当前[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource)对象代表订单表，它有一个当前的订单记录。接下来，Aspose.Words 在文档中遇到“MERGEFIELD TableStart:OrderDetails”并调用[getChildDataSource(java.lang.String)](../../com.aspose.words/imailmergedatasource\#getChildDataSource-java.lang.String-).您需要创建并返回一个[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource)允许 Aspose.Words 访问当前订单的 OrderDetails 记录的对象。

如果此数据源对象与指定名称的表没有关系，则需要返回一个[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource)将提供对指定表的所有记录的访问的对象。

如果具有指定名称的表不存在，您的实现应返回 null 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tableName | java.lang.String | 模板文档中指定的邮件合并区域的名称。不区分大小写。 |

**退货:**
[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) - 将提供对指定表的数据记录的访问的数据源对象。
### getTableName() {#getTableName--}
```
public abstract String getTableName()
```


返回数据源的名称。

如果你正在实施[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource)从此属性返回数据源的名称。

Aspose.Words 使用这个名称来匹配模板文档中指定的邮件合并区域名称。数据源名称和邮件合并区域名称之间的比较不区分大小写。

**退货:**
java.lang.String - 数据源的名称。如果数据源没有名称，则为空字符串。
### getValue(String fieldName, Ref fieldValue) {#getValue-java.lang.String-com.aspose.words.ref.Ref-}
```
public abstract boolean getValue(String fieldName, Ref fieldValue)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldName | java.lang.String |  |
| fieldValue | [Ref](../../com.aspose.words.ref/ref) |  |

**退货:**
布尔值
### moveNext() {#moveNext--}
```
public abstract boolean moveNext()
```


前进到数据源中的下一条记录。

**退货:**
布尔值 - 如果成功移动到下一条记录则为真。如果到达数据源末尾则为假。