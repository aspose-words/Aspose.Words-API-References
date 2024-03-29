---
title: MailMergeSettings
second_title: Aspose.Words for Java API 参考
description: 指定文档的所有邮件合并信息。
type: docs
weight: 386
url: /zh/java/com.aspose.words/mailmergesettings/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Cloneable
```
public class MailMergeSettings implements Cloneable
```

指定文档的所有邮件合并信息。

要了解更多信息，请访问**Mail Merge and Reporting**文档文章。

您可以使用此对象为文档指定邮件合并数据源，当用户打开此文档时，此信息（连同可用的数据字段）将出现在 Microsoft Word 中。或者，您可以使用此对象查询用户在 Microsoft Word 中为此文档指定的邮件合并设置。

您通常不需要直接创建此类的对象，因为文档的邮件合并设置始终可以通过[Document.getMailMergeSettings()](../../com.aspose.words/document\#getMailMergeSettings--) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document\#setMailMergeSettings-com.aspose.words.MailMergeSettings-)财产。

要检测此文档是否为邮件合并主文档，请检查[getMainDocumentType()](../../com.aspose.words/mailmergesettings\#getMainDocumentType--) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings\#setMainDocumentType-int-)财产。

要从文档中删除邮件合并设置和数据源信息，您可以使用[clear()](../../com.aspose.words/mailmergesettings\#clear--)方法。 Aspose.Words 不会将邮件合并设置写入文档，如果[getMainDocumentType()](../../com.aspose.words/mailmergesettings\#getMainDocumentType--) / [setMainDocumentType(int)](../../com.aspose.words/mailmergesettings\#setMainDocumentType-int-)属性设置为[MailMergeMainDocumentType.NOT\_A\_MERGE\_DOCUMENT](../../com.aspose.words/mailmergemaindocumenttype\#NOT-A-MERGE-DOCUMENT)或者[getDataType()](../../com.aspose.words/mailmergesettings\#getDataType--) / [setDataType(int)](../../com.aspose.words/mailmergesettings\#setDataType-int-)属性设置为[MailMergeDataType.NONE](../../com.aspose.words/mailmergedatatype\#NONE).

学习如何使用该对象的属性的最佳方法是在 Microsoft Word 中手动创建一个包含所需数据源的文档，然后使用 Aspose.Words 打开该文档并检查该对象的属性[Document.getMailMergeSettings()](../../com.aspose.words/document\#getMailMergeSettings--) / [Document.setMailMergeSettings(com.aspose.words.MailMergeSettings)](../../com.aspose.words/document\#setMailMergeSettings-com.aspose.words.MailMergeSettings-)和[getOdso()](../../com.aspose.words/mailmergesettings\#getOdso--) / [setOdso(com.aspose.words.Odso)](../../com.aspose.words/mailmergesettings\#setOdso-com.aspose.words.Odso-)对象。例如，如果您想学习如何以编程方式配置数据源，这是一个很好的方法。

 Aspose.Words 在不同格式之间加载、保存和转换文档时保留邮件合并信息，但在使用[MailMerge](../../com.aspose.words/mailmerge)目的。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clear()](#clear--) | 以这样的方式清除邮件合并设置，即在保存文档时，不保存任何邮件合并设置，它将成为一个普通文档。 |
| [deepClone()](#deepClone--) | 返回此对象的深度克隆。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getActiveRecord()](#getActiveRecord--) | 指定应在 Microsoft Word 中显示的数据源记录的从一开始的索引。 |
| [getAddressFieldName()](#getAddressFieldName--) | 指定数据源中包含电子邮件地址的列。 |
| [getCheckErrors()](#getCheckErrors--) | 指定在执行邮件合并时应由 Microsoft Word 执行的错误报告类型。 |
| [getClass()](#getClass--) |  |
| [getConnectString()](#getConnectString--) | 指定用于连接到外部数据源的连接字符串。 |
| [getDataSource()](#getDataSource--) | 指定邮件合并数据源的路径。 |
| [getDataType()](#getDataType--) | 指定邮件合并数据源的类型和数据访问方法。 |
| [getDestination()](#getDestination--) | 指定 Microsoft Word 如何输出邮件合并的结果。 |
| [getDoNotSupressBlankLines()](#getDoNotSupressBlankLines--) | 指定执行邮件合并的应用程序应如何处理邮件合并产生的合并文档中的空行。 |
| [getHeaderSource()](#getHeaderSource--) | 指定邮件合并标头源的路径。 |
| [getLinkToQuery()](#getLinkToQuery--) | 不确定这个。 |
| [getMailAsAttachment()](#getMailAsAttachment--) | 指定在邮件合并操作期间生成的文档应作为附件而不是实际电子邮件的正文通过电子邮件发送。 |
| [getMailSubject()](#getMailSubject--) | 指定应出现在邮件合并期间生成的电子邮件或传真的主题行中的文本。 |
| [getMainDocumentType()](#getMainDocumentType--) | 指定邮件合并主文档类型。 |
| [getOdso()](#getOdso--) | 获取指定 Office 数据源对象 (ODSO) 设置的对象。 |
| [getQuery()](#getQuery--) | 包含应针对指定外部数据源运行的结构化查询语言字符串，以返回执行邮件合并操作时应导入文档的记录集。 |
| [getViewMergedData()](#getViewMergedData--) | 指定 Microsoft Word 应显示来自已插入合并字段的指定外部数据源的数据（例如 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setActiveRecord(int value)](#setActiveRecord-int-) | 指定应在 Microsoft Word 中显示的数据源记录的从一开始的索引。 |
| [setAddressFieldName(String value)](#setAddressFieldName-java.lang.String-) | 指定数据源中包含电子邮件地址的列。 |
| [setCheckErrors(int value)](#setCheckErrors-int-) | 指定在执行邮件合并时应由 Microsoft Word 执行的错误报告类型。 |
| [setConnectString(String value)](#setConnectString-java.lang.String-) | 指定用于连接到外部数据源的连接字符串。 |
| [setDataSource(String value)](#setDataSource-java.lang.String-) | 指定邮件合并数据源的路径。 |
| [setDataType(int value)](#setDataType-int-) | 指定邮件合并数据源的类型和数据访问方法。 |
| [setDestination(int value)](#setDestination-int-) | 指定 Microsoft Word 如何输出邮件合并的结果。 |
| [setDoNotSupressBlankLines(boolean value)](#setDoNotSupressBlankLines-boolean-) | 指定执行邮件合并的应用程序应如何处理邮件合并产生的合并文档中的空行。 |
| [setHeaderSource(String value)](#setHeaderSource-java.lang.String-) | 指定邮件合并标头源的路径。 |
| [setLinkToQuery(boolean value)](#setLinkToQuery-boolean-) | 不确定这个。 |
| [setMailAsAttachment(boolean value)](#setMailAsAttachment-boolean-) | 指定在邮件合并操作期间生成的文档应作为附件而不是实际电子邮件的正文通过电子邮件发送。 |
| [setMailSubject(String value)](#setMailSubject-java.lang.String-) | 指定应出现在邮件合并期间生成的电子邮件或传真的主题行中的文本。 |
| [setMainDocumentType(int value)](#setMainDocumentType-int-) | 指定邮件合并主文档类型。 |
| [setOdso(Odso value)](#setOdso-com.aspose.words.Odso-) | 设置指定 Office 数据源对象 (ODSO) 设置的对象。 |
| [setQuery(String value)](#setQuery-java.lang.String-) | 包含应针对指定外部数据源运行的结构化查询语言字符串，以返回执行邮件合并操作时应导入文档的记录集。 |
| [setViewMergedData(boolean value)](#setViewMergedData-boolean-) | 指定 Microsoft Word 应显示来自已插入合并字段的指定外部数据源的数据（例如 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clear() {#clear--}
```
public void clear()
```


以这样的方式清除邮件合并设置，即在保存文档时，不保存任何邮件合并设置，它将成为一个普通文档。

### deepClone() {#deepClone--}
```
public MailMergeSettings deepClone()
```


返回此对象的深度克隆。

**退货：**
[MailMergeSettings](../../com.aspose.words/mailmergesettings)
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getActiveRecord() {#getActiveRecord--}
```
public int getActiveRecord()
```


指定应在 Microsoft Word 中显示的数据源记录的从一开始的索引。默认值为 1。

**退货：**
int - 相应的 int 值。
### getAddressFieldName() {#getAddressFieldName--}
```
public String getAddressFieldName()
```


指定数据源中包含电子邮件地址的列。默认值为空字符串。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getCheckErrors() {#getCheckErrors--}
```
public int getCheckErrors()
```


指定在执行邮件合并时应由 Microsoft Word 执行的错误报告类型。默认值为[MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors\#DEFAULT).

**退货：**
int - 相应的 int 值。返回值是其中之一[MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors)常数。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getConnectString() {#getConnectString--}
```
public String getConnectString()
```


指定用于连接到外部数据源的连接字符串。默认值为空字符串。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getDataSource() {#getDataSource--}
```
public String getDataSource()
```


指定邮件合并数据源的路径。默认值为空字符串。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getDataType() {#getDataType--}
```
public int getDataType()
```


指定邮件合并数据源的类型和数据访问方法。默认值为[MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype\#DEFAULT).

**退货：**
int - 相应的 int 值。返回值是其中之一[MailMergeDataType](../../com.aspose.words/mailmergedatatype)常数。
### getDestination() {#getDestination--}
```
public int getDestination()
```


指定 Microsoft Word 如何输出邮件合并的结果。默认值为[MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination\#DEFAULT).

**退货：**
int - 相应的 int 值。返回值是其中之一[MailMergeDestination](../../com.aspose.words/mailmergedestination)常数。
### getDoNotSupressBlankLines() {#getDoNotSupressBlankLines--}
```
public boolean getDoNotSupressBlankLines()
```


指定执行邮件合并的应用程序应如何处理邮件合并产生的合并文档中的空行。默认值为 false 。

**退货：**
boolean - 相应的布尔值。
### getHeaderSource() {#getHeaderSource--}
```
public String getHeaderSource()
```


指定邮件合并标头源的路径。默认值为空字符串。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getLinkToQuery() {#getLinkToQuery--}
```
public boolean getLinkToQuery()
```


不确定这个。 Microsoft Word 自动化参考建议这指定每次在 Microsoft Word 中打开文档时都会执行查询。但是 OOXML 规范建议这指定查询包含对包含实际查询的外部查询文件的引用。默认值为 false 。

**退货：**
boolean - 相应的布尔值。
### getMailAsAttachment() {#getMailAsAttachment--}
```
public boolean getMailAsAttachment()
```


指定在邮件合并操作期间生成的文档应作为附件而不是实际电子邮件的正文通过电子邮件发送。默认值为 false 。

**退货：**
boolean - 相应的布尔值。
### getMailSubject() {#getMailSubject--}
```
public String getMailSubject()
```


指定应出现在邮件合并期间生成的电子邮件或传真的主题行中的文本。默认值为空字符串。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getMainDocumentType() {#getMainDocumentType--}
```
public int getMainDocumentType()
```


指定邮件合并主文档类型。默认值为[MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype\#DEFAULT).

主文档是包含对于合并文档的每个版本都相同的信息的文档。

**退货：**
int - 相应的 int 值。返回值是其中之一[MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype)常数。
### getOdso() {#getOdso--}
```
public Odso getOdso()
```


获取指定 Office 数据源对象 (ODSO) 设置的对象。

该对象永远不会为空。

**退货：**
[Odso](../../com.aspose.words/odso) - 指定 Office 数据源对象 (ODSO) 设置的对象。
### getQuery() {#getQuery--}
```
public String getQuery()
```


包含应针对指定外部数据源运行的结构化查询语言字符串，以返回执行邮件合并操作时应导入文档的记录集。默认值为空字符串。

**退货：**
java.lang.String - 相应的 java.lang.String 值。
### getViewMergedData() {#getViewMergedData--}
```
public boolean getViewMergedData()
```


指定 Microsoft Word 应显示来自已插入合并字段的指定外部数据源的数据（例如预览合并数据）。默认值为 false 。

**退货：**
boolean - 相应的布尔值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setActiveRecord(int value) {#setActiveRecord-int-}
```
public void setActiveRecord(int value)
```


指定应在 Microsoft Word 中显示的数据源记录的从一开始的索引。默认值为 1。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。 |

### setAddressFieldName(String value) {#setAddressFieldName-java.lang.String-}
```
public void setAddressFieldName(String value)
```


指定数据源中包含电子邮件地址的列。默认值为空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setCheckErrors(int value) {#setCheckErrors-int-}
```
public void setCheckErrors(int value)
```


指定在执行邮件合并时应由 Microsoft Word 执行的错误报告类型。默认值为[MailMergeCheckErrors.DEFAULT](../../com.aspose.words/mailmergecheckerrors\#DEFAULT).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[MailMergeCheckErrors](../../com.aspose.words/mailmergecheckerrors)常数。 |

### setConnectString(String value) {#setConnectString-java.lang.String-}
```
public void setConnectString(String value)
```


指定用于连接到外部数据源的连接字符串。默认值为空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setDataSource(String value) {#setDataSource-java.lang.String-}
```
public void setDataSource(String value)
```


指定邮件合并数据源的路径。默认值为空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setDataType(int value) {#setDataType-int-}
```
public void setDataType(int value)
```


指定邮件合并数据源的类型和数据访问方法。默认值为[MailMergeDataType.DEFAULT](../../com.aspose.words/mailmergedatatype\#DEFAULT).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[MailMergeDataType](../../com.aspose.words/mailmergedatatype)常数。 |

### setDestination(int value) {#setDestination-int-}
```
public void setDestination(int value)
```


指定 Microsoft Word 如何输出邮件合并的结果。默认值为[MailMergeDestination.DEFAULT](../../com.aspose.words/mailmergedestination\#DEFAULT).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[MailMergeDestination](../../com.aspose.words/mailmergedestination)常数。 |

### setDoNotSupressBlankLines(boolean value) {#setDoNotSupressBlankLines-boolean-}
```
public void setDoNotSupressBlankLines(boolean value)
```


指定执行邮件合并的应用程序应如何处理邮件合并产生的合并文档中的空行。默认值为 false 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setHeaderSource(String value) {#setHeaderSource-java.lang.String-}
```
public void setHeaderSource(String value)
```


指定邮件合并标头源的路径。默认值为空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setLinkToQuery(boolean value) {#setLinkToQuery-boolean-}
```
public void setLinkToQuery(boolean value)
```


不确定这个。 Microsoft Word 自动化参考建议这指定每次在 Microsoft Word 中打开文档时都会执行查询。但是 OOXML 规范建议这指定查询包含对包含实际查询的外部查询文件的引用。默认值为 false 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setMailAsAttachment(boolean value) {#setMailAsAttachment-boolean-}
```
public void setMailAsAttachment(boolean value)
```


指定在邮件合并操作期间生成的文档应作为附件而不是实际电子邮件的正文通过电子邮件发送。默认值为 false 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setMailSubject(String value) {#setMailSubject-java.lang.String-}
```
public void setMailSubject(String value)
```


指定应出现在邮件合并期间生成的电子邮件或传真的主题行中的文本。默认值为空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setMainDocumentType(int value) {#setMainDocumentType-int-}
```
public void setMainDocumentType(int value)
```


指定邮件合并主文档类型。默认值为[MailMergeMainDocumentType.DEFAULT](../../com.aspose.words/mailmergemaindocumenttype\#DEFAULT).

主文档是包含对于合并文档的每个版本都相同的信息的文档。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的int值。该值必须是其中之一[MailMergeMainDocumentType](../../com.aspose.words/mailmergemaindocumenttype)常数。 |

### setOdso(Odso value) {#setOdso-com.aspose.words.Odso-}
```
public void setOdso(Odso value)
```


设置指定 Office 数据源对象 (ODSO) 设置的对象。

该对象永远不会为空。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [Odso](../../com.aspose.words/odso) | 指定 Office 数据源对象 (ODSO) 设置的对象。 |

### setQuery(String value) {#setQuery-java.lang.String-}
```
public void setQuery(String value)
```


包含应针对指定外部数据源运行的结构化查询语言字符串，以返回执行邮件合并操作时应导入文档的记录集。默认值为空字符串。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 对应的java.lang.String值。 |

### setViewMergedData(boolean value) {#setViewMergedData-boolean-}
```
public void setViewMergedData(boolean value)
```


指定 Microsoft Word 应显示来自已插入合并字段的指定外部数据源的数据（例如预览合并数据）。默认值为 false 。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
