---
title: Odso
second_title: Aspose.Words for Java API Reference
description: 指定邮件合并数据源的 Office 数据源对象 ODSO 设置。
type: docs
weight: 411
url: /zh/java/com.aspose.words/odso/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Cloneable
```
public class Odso implements Cloneable
```

指定邮件合并数据源的 Office 数据源对象 (ODSO) 设置。

要了解更多信息，请访问**Mail Merge and Reporting**文档文章。

ODSO 似乎是较新的 Microsoft Word 版本在为邮件合并文档指定某些类型的数据源时更喜欢使用的“新”方式。 ODSO 可能首先出现在 Microsoft Word 2000 中。

ODSO 的使用文档很少，学习如何使用此对象的属性的最佳方法是在 Microsoft Word 中手动创建具有所需数据源的文档，然后使用 Aspose.Words 打开该文档并检查该对象的属性[Document.getMailMergeSettings()](../../com.aspose.words/document\#getMailMergeSettings--) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document\#setMailMergeSettings-com.aspose.words.MailMergeSettings-)和[MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings\#getOdso--) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings\#setOdso-com.aspose.words.Odso-)对象。例如，如果您想学习如何以编程方式配置数据源，这是一个很好的方法。

您通常不需要直接创建此类的对象，因为 ODSO 设置始终可以通过[MailMergeSettings.getOdso()](../../com.aspose.words/mailmergesettings\#getOdso--) / [MailMergeSettings.setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings\#setOdso-com.aspose.words.Odso-)财产。
## 方法

| 方法 | 描述 |
| --- | --- |
| [deepClone()](#deepClone--) | 返回此对象的深层克隆。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getColumnDelimiter()](#getColumnDelimiter--) | 指定应解释为用于分隔外部数据源中的列的列分隔符的字符。 |
| [getDataSource()](#getDataSource--) | 指定要连接到文档以执行邮件合并的外部数据源的位置。 |
| [getDataSource类型()](#getDataSource类型--) | 指定要连接到的外部数据源的类型，作为此邮件合并的 ODSO 连接信息的一部分。 |
| [get字段MapDatas()](#get字段MapDatas--) | 获取一组对象，这些对象指定来自外部数据源的列如何映射到文档中预定义的合并字段名称。 |
| [getFirstRowContainsColumnNames()](#getFirstRowContainsColumnNames--) | 指定托管应用程序应将指定外部数据源中的第一行数据视为包含数据源中每一列名称的标题行。 |
| [getRecipientDatas()](#getRecipientDatas--) | 获取指定邮件合并中单个记录的包含/排除的对象集合。 |
| [getTableName()](#getTableName--) | 指定源应连接到外部数据源中的特定数据集。 |
| [getUdlConnectString()](#getUdlConnectString--) | 指定用于连接到外部数据源的通用数据链接 (UDL) 连接字符串。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setColumnDelimiter(char value)](#setColumnDelimiter-char-) | 指定应解释为用于分隔外部数据源中的列的列分隔符的字符。 |
| [setDataSource(String value)](#setDataSource-java.lang.String-) | 指定要连接到文档以执行邮件合并的外部数据源的位置。 |
| [setDataSource类型(int value)](#setDataSource类型-int-) | 指定要连接到的外部数据源的类型，作为此邮件合并的 ODSO 连接信息的一部分。 |
| [set字段MapDatas(Odso字段MapDataCollection value)](#set字段MapDatas-com.aspose.words.Odso字段MapDataCollection-) | 设置一组对象，这些对象指定来自外部数据源的列如何映射到文档中的预定义合并字段名称。 |
| [setFirstRowContainsColumnNames(boolean value)](#setFirstRowContainsColumnNames-boolean-) | 指定托管应用程序应将指定外部数据源中的第一行数据视为包含数据源中每一列名称的标题行。 |
| [setRecipientDatas(OdsoRecipientDataCollection value)](#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection-) | 设置指定邮件合并中单个记录的包含/排除的对象集合。 |
| [setTableName(String value)](#setTableName-java.lang.String-) | 指定源应连接到外部数据源中的特定数据集。 |
| [setUdlConnectString(String value)](#setUdlConnectString-java.lang.String-) | 指定用于连接到外部数据源的通用数据链接 (UDL) 连接字符串。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### deepClone() {#deepClone--}
```
public Odso deepClone()
```


返回此对象的深层克隆。

**退货:**
[Odso](../../com.aspose.words/odso)
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getColumnDelimiter() {#getColumnDelimiter--}
```
public char getColumnDelimiter()
```


指定应解释为用于分隔外部数据源中的列的列分隔符的字符。默认值为 0，这意味着没有定义列分隔符。

RK 我从来没有见过这个在使用中。

**退货:**
char - 对应的 char 值。
### getDataSource() {#getDataSource--}
```
public String getDataSource()
```


指定要连接到文档以执行邮件合并的外部数据源的位置。默认值为空字符串。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getDataSource类型() {#getDataSource类型--}
```
public int getDataSource类型()
```


指定要连接到的外部数据源的类型，作为此邮件合并的 ODSO 连接信息的一部分。默认值为[OdsoDataSource类型.DEFAULT](../../com.aspose.words/odsodatasourcetype\#DEFAULT).

此设置纯粹是用于此邮件合并的数据源类型的建议。

**退货:**
int - 对应的 int 值。返回值是以下之一[OdsoDataSource类型](../../com.aspose.words/odsodatasourcetype)常数。
### get字段MapDatas() {#get字段MapDatas--}
```
public Odso字段MapDataCollection get字段MapDatas()
```


获取一组对象，这些对象指定来自外部数据源的列如何映射到文档中预定义的合并字段名称。该对象永远不会为空。

**退货:**
[Odso字段MapDataCollection](../../com.aspose.words/odsofieldmapdatacollection) - 一组对象，它们指定来自外部数据源的列如何映射到文档中预定义的合并字段名称。
### getFirstRowContainsColumnNames() {#getFirstRowContainsColumnNames--}
```
public boolean getFirstRowContainsColumnNames()
```


指定托管应用程序应将指定外部数据源中的第一行数据视为包含数据源中每一列名称的标题行。默认值为 false 。

RK 我从来没有见过这个在使用中。

**退货:**
boolean - 对应的布尔值。
### getRecipientDatas() {#getRecipientDatas--}
```
public OdsoRecipientDataCollection getRecipientDatas()
```


获取指定邮件合并中单个记录的包含/排除的对象集合。该对象永远不会为空。

**退货:**
[OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection) - 指定在邮件合并中包含/排除单个记录的对象集合。
### getTableName() {#getTableName--}
```
public String getTableName()
```


指定源应连接到外部数据源中的特定数据集。默认值为空字符串。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### getUdlConnectString() {#getUdlConnectString--}
```
public String getUdlConnectString()
```


指定用于连接到外部数据源的通用数据链接 (UDL) 连接字符串。默认值为空字符串。

**退货:**
java.lang.String - 对应的 java.lang.String 值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setColumnDelimiter(char value) {#setColumnDelimiter-char-}
```
public void setColumnDelimiter(char value)
```


指定应解释为用于分隔外部数据源中的列的列分隔符的字符。默认值为 0，这意味着没有定义列分隔符。

RK 我从来没有见过这个在使用中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | char | 对应的 char 值。 |

### setDataSource(String value) {#setDataSource-java.lang.String-}
```
public void setDataSource(String value)
```


指定要连接到文档以执行邮件合并的外部数据源的位置。默认值为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setDataSource类型(int value) {#setDataSource类型-int-}
```
public void setDataSource类型(int value)
```


指定要连接到的外部数据源的类型，作为此邮件合并的 ODSO 连接信息的一部分。默认值为[OdsoDataSource类型.DEFAULT](../../com.aspose.words/odsodatasourcetype\#DEFAULT).

此设置纯粹是用于此邮件合并的数据源类型的建议。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[OdsoDataSource类型](../../com.aspose.words/odsodatasourcetype)常数。 |

### set字段MapDatas(Odso字段MapDataCollection value) {#set字段MapDatas-com.aspose.words.Odso字段MapDataCollection-}
```
public void set字段MapDatas(Odso字段MapDataCollection value)
```


设置一组对象，这些对象指定来自外部数据源的列如何映射到文档中的预定义合并字段名称。该对象永远不会为空。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Odso字段MapDataCollection](../../com.aspose.words/odsofieldmapdatacollection) | 一组对象，它们指定来自外部数据源的列如何映射到文档中预定义的合并字段名称。 |

### setFirstRowContainsColumnNames(boolean value) {#setFirstRowContainsColumnNames-boolean-}
```
public void setFirstRowContainsColumnNames(boolean value)
```


指定托管应用程序应将指定外部数据源中的第一行数据视为包含数据源中每一列名称的标题行。默认值为 false 。

RK 我从来没有见过这个在使用中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setRecipientDatas(OdsoRecipientDataCollection value) {#setRecipientDatas-com.aspose.words.OdsoRecipientDataCollection-}
```
public void setRecipientDatas(OdsoRecipientDataCollection value)
```


设置指定邮件合并中单个记录的包含/排除的对象集合。该对象永远不会为空。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [OdsoRecipientDataCollection](../../com.aspose.words/odsorecipientdatacollection) | 指定在邮件合并中包含/排除单个记录的对象集合。 |

### setTableName(String value) {#setTableName-java.lang.String-}
```
public void setTableName(String value)
```


指定源应连接到外部数据源中的特定数据集。默认值为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### setUdlConnectString(String value) {#setUdlConnectString-java.lang.String-}
```
public void setUdlConnectString(String value)
```


指定用于连接到外部数据源的通用数据链接 (UDL) 连接字符串。默认值为空字符串。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的 java.lang.String 值。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
