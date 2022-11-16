---
title: MailMerge
second_title: Aspose.Words for Java API 参考
description: 表示邮件合并功能。
type: docs
weight: 379
url: /zh/java/com.aspose.words/mailmerge/
---

**遗产：**
java.lang.Object
```
public class MailMerge
```

表示邮件合并功能。

要了解更多信息，请访问**Mail Merge and Reporting**文档文章。

要使邮件合并操作正常工作，文档应包含 Word MERGEFIELD 和可选的 NEXT 字段。在邮件合并操作期间，文档中的合并字段将替换为数据源中的值。

使用邮件合并有两种不同的方式：使用邮件合并区域和不使用邮件合并区域。

最简单的邮件合并是没有区域的，它与 Word 中邮件合并的工作方式非常相似。使用 Execute 方法来合并来自某些数据源的信息，例如**DataTable**, **DataSet**或将一组对象放入您的文档中。这**MailMerge**对象处理数据源的所有记录，并为每条记录复制和附加整个文档的内容。

请注意，当**MailMerge**对象遇到 NEXT 字段，它选择数据源中的下一条记录并继续合并而不复制任何内容。

使用 ExecuteWithRegions 方法将信息合并到定义了邮件合并区域的文档中。您可以使用 或 作为此操作的数据源。

如果您想在文档中动态增长部分，则需要使用邮件合并区域。如果没有邮件合并区域，整个文档将针对数据源的每条记录重复。
## 方法

| 方法 | 描述 |
| --- | --- |
| [deleteFields()](#deleteFields--) | 从文档中删除邮件合并相关字段。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [execute(IMailMergeDataSource dataSource)](#execute-com.aspose.words.IMailMergeDataSource-) | 从自定义数据源执行邮件合并。 |
| [execute(System.Data.DataRow row)](#execute-com.aspose.words.net.System.Data.DataRow-) | 执行从 DataRow 到文档的邮件合并。 |
| [execute(System.Data.DataTable table)](#execute-com.aspose.words.net.System.Data.DataTable-) | 执行从 com.aspose.words.net.System.Data.DataTable 到文档的邮件合并。 |
| [execute(System.Data.DataView dataView)](#execute-com.aspose.words.net.System.Data.DataView-) | 执行从 DataView 到文档的邮件合并。 |
| [execute(System.Data.IDataReader dataReader)](#execute-com.aspose.words.net.System.Data.IDataReader-) | 执行从 IDataReader 到文档的邮件合并。 |
| [execute(String[] fieldNames, Object[] values)](#execute-java.lang.String---java.lang.Object---) | 执行邮件合并操作。 |
| [executeWithRegions(IMailMergeDataSource dataSource)](#executeWithRegions-com.aspose.words.IMailMergeDataSource-) | 从具有邮件合并区域的自定义数据源执行邮件合并。 |
| [executeWithRegions(IMailMergeDataSourceRoot dataSourceRoot)](#executeWithRegions-com.aspose.words.IMailMergeDataSourceRoot-) | 从具有邮件合并区域的自定义数据源执行邮件合并。 |
| [executeWithRegions(System.Data.DataSet dataSet)](#executeWithRegions-com.aspose.words.net.System.Data.DataSet-) | 对具有邮件合并区域的文档执行邮件合并操作。 |
| [executeWithRegions(System.Data.DataTable dataTable)](#executeWithRegions-com.aspose.words.net.System.Data.DataTable-) | 执行从 DataTable 到具有邮件合并区域的文档的邮件合并。 |
| [executeWithRegions(System.Data.DataView dataView)](#executeWithRegions-com.aspose.words.net.System.Data.DataView-) | 执行从 DataView 到具有邮件合并区域的文档的邮件合并。 |
| [executeWithRegions(System.Data.IDataReader dataReader, String tableName)](#executeWithRegions-com.aspose.words.net.System.Data.IDataReader-java.lang.String-) | 执行从 IDataReader 到具有邮件合并区域的文档的邮件合并。 |
| [getClass()](#getClass--) |  |
| [getCleanupOptions()](#getCleanupOptions--) | 获取一组标志，这些标志指定在邮件合并期间应删除哪些项目。 |
| [getCleanupParagraphsWithPunctuationMarks()](#getCleanupParagraphsWithPunctuationMarks--) | 获取一个值，该值指示带有标点符号的段落是否被视为空，如果[MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-EMPTY-PARAGRAPHS)选项被指定。 |
| [getFieldMergingCallback()](#getFieldMergingCallback--) | 当在文档中遇到邮件合并字段时，在邮件合并期间发生。 |
| [getFieldNames()](#getFieldNames--) | 返回文档中可用的邮件合并字段名称的集合。 |
| [getFieldNamesForRegion(String regionName)](#getFieldNamesForRegion-java.lang.String-) | 从区域获取邮件合并字段名称。 |
| [getFieldNamesForRegion(String regionName, int regionIndex)](#getFieldNamesForRegion-java.lang.String-int-) | 返回区域中可用的邮件合并字段名称的集合。 |
| [getMailMergeCallback()](#getMailMergeCallback--) | 允许在邮件合并期间处理特定事件。 |
| [getMappedDataFields()](#getMappedDataFields--) | 返回表示邮件合并操作的映射数据字段的集合。 |
| [getMergeDuplicateRegions()](#getMergeDuplicateRegions--) | 获取一个值，该值指示在针对数据源或仅第一个区域执行邮件合并时，是否应合并所有具有数据源名称的文档邮件合并区域。 |
| [getMergeWholeDocument()](#getMergeWholeDocument--) | 获取一个值，该值指示在执行区域邮件合并时是否更新整个文档中的字段。 |
| [getPreserveUnusedTags()](#getPreserveUnusedTags--) | 获取一个值，该值指示是否应保留未使用的“小胡子”标签。 |
| [getRegionEndTag()](#getRegionEndTag--) | 获取邮件合并区域结束标记。 |
| [getRegionStartTag()](#getRegionStartTag--) | 获取邮件合并区域开始标记。 |
| [getRegionsByName(String regionName)](#getRegionsByName-java.lang.String-) | 返回具有指定名称的邮件合并区域的集合。 |
| [getRegionsHierarchy()](#getRegionsHierarchy--) | 返回文档中可用区域（带有字段）的完整层次结构。 |
| [getRestartListsAtEachSection()](#getRestartListsAtEachSection--) | 获取一个值，该值指示在执行邮件合并后是否在每个部分重新启动列表。 |
| [getRetainFirstSectionStart()](#getRetainFirstSectionStart--) | 获取一个值，该值指示是否[PageSetup.getSectionStart()](../../com.aspose.words/pagesetup\#getSectionStart--) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup\#setSectionStart-int-)第一个文档部分及其后续数据源行的副本在邮件合并期间保留或根据 MS Word 行为更新。 |
| [getTrimWhitespaces()](#getTrimWhitespaces--) | 获取一个值，该值指示是否从邮件合并值中删除尾随和前导空格。 |
| [getUnconditionalMergeFieldsAndRegions()](#getUnconditionalMergeFieldsAndRegions--) | 获取一个值，该值指示是否合并合并字段和合并区域，而不管父 IF 字段的条件如何。 |
| [getUseNonMergeFields()](#getUseNonMergeFields--) | 当为 true 时，指定除了 MERGEFIELD 字段之外，邮件合并被执行到一些其他类型的字段中，也被执行到“\{\{字段名\}\}”标签。 |
| [getUseWholeParagraphAsRegion()](#getUseWholeParagraphAsRegion--) | 获取一个值，该值指示是否应将具有 TableStart 或 TableEnd 字段的整个段落或 TableStart 和 TableEnd 字段之间的特定范围包含到邮件合并区域中。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setCleanupOptions(int value)](#setCleanupOptions-int-) | 设置一组标志，指定在邮件合并期间应删除哪些项目。 |
| [setCleanupParagraphsWithPunctuationMarks(boolean value)](#setCleanupParagraphsWithPunctuationMarks-boolean-) | 设置一个值，指示带标点符号的段落是否被视为空的，如果[MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-EMPTY-PARAGRAPHS)选项被指定。 |
| [setFieldMergingCallback(IFieldMergingCallback value)](#setFieldMergingCallback-com.aspose.words.IFieldMergingCallback-) | 当在文档中遇到邮件合并字段时，在邮件合并期间发生。 |
| [setMailMergeCallback(IMailMergeCallback value)](#setMailMergeCallback-com.aspose.words.IMailMergeCallback-) | 允许在邮件合并期间处理特定事件。 |
| [setMergeDuplicateRegions(boolean value)](#setMergeDuplicateRegions-boolean-) | 设置一个值，该值指示在针对数据源或仅第一个区域执行邮件合并时，是否应合并所有具有数据源名称的文档邮件合并区域。 |
| [setMergeWholeDocument(boolean value)](#setMergeWholeDocument-boolean-) | 设置一个值，指示在执行与区域的邮件合并时是否更新整个文档中的字段。 |
| [setPreserveUnusedTags(boolean value)](#setPreserveUnusedTags-boolean-) | 设置一个值，指示是否应保留未使用的“小胡子”标签。 |
| [setRegionEndTag(String value)](#setRegionEndTag-java.lang.String-) | 设置邮件合并区域结束标记。 |
| [setRegionStartTag(String value)](#setRegionStartTag-java.lang.String-) | 设置邮件合并区域开始标记。 |
| [setRestartListsAtEachSection(boolean value)](#setRestartListsAtEachSection-boolean-) | 设置一个值，该值指示在执行邮件合并后是否在每个部分重新启动列表。 |
| [setRetainFirstSectionStart(boolean value)](#setRetainFirstSectionStart-boolean-) | 设置一个值，指示是否[PageSetup.getSectionStart()](../../com.aspose.words/pagesetup\#getSectionStart--) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup\#setSectionStart-int-)第一个文档部分及其后续数据源行的副本在邮件合并期间保留或根据 MS Word 行为更新。 |
| [setTrimWhitespaces(boolean value)](#setTrimWhitespaces-boolean-) | 设置一个值，该值指示是否从邮件合并值中删除尾随和前导空格。 |
| [setUnconditionalMergeFieldsAndRegions(boolean value)](#setUnconditionalMergeFieldsAndRegions-boolean-) | 设置一个值，指示是否合并合并字段和合并区域，而不管父 IF 字段的条件如何。 |
| [setUseNonMergeFields(boolean value)](#setUseNonMergeFields-boolean-) | 当为 true 时，指定除了 MERGEFIELD 字段之外，邮件合并被执行到一些其他类型的字段中，也被执行到“\{\{字段名\}\}”标签。 |
| [setUseWholeParagraphAsRegion(boolean value)](#setUseWholeParagraphAsRegion-boolean-) | 设置一个值，指示是否应将具有 TableStart 或 TableEnd 字段的整个段落或 TableStart 和 TableEnd 字段之间的特定范围包含到邮件合并区域中。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### deleteFields() {#deleteFields--}
```
public void deleteFields()
```


从文档中删除邮件合并相关字段。

此方法从文档中删除 MERGEFIELD 和 NEXT 字段。

如果您的邮件合并操作并不总是需要填充文档中的所有字段，则此方法可能很有用。使用此方法删除所有剩余的邮件合并字段。

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
### execute(IMailMergeDataSource dataSource) {#execute-com.aspose.words.IMailMergeDataSource-}
```
public void execute(IMailMergeDataSource dataSource)
```


从自定义数据源执行邮件合并。

使用此方法可以使用来自任何数据源（例如列表或哈希表或对象）的值填充文档中的邮件合并字段。您需要编写自己的类来实现[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource)界面。

您只能在以下情况下使用此方法[FieldOptions.isBidiTextSupportedOnUpdate()](../../com.aspose.words/fieldoptions\#isBidiTextSupportedOnUpdate--) / [FieldOptions.isBidiTextSupportedOnUpdate(boolean)](../../com.aspose.words/fieldoptions\#isBidiTextSupportedOnUpdate-boolean-)是假的，也就是说你不需要从右到左的语言（如阿拉伯语或希伯来语）兼容性。

该方法忽略了[MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-UNUSED-REGIONS)选项。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataSource | [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) | 实现自定义邮件合并数据源接口的对象。 |

### execute(System.Data.DataRow row) {#execute-com.aspose.words.net.System.Data.DataRow-}
```
public void execute(System.Data.DataRow row)
```


执行从 DataRow 到文档的邮件合并。

使用此方法用来自 a 的值填充文档中的邮件合并字段**DataRow**.

该方法忽略了[MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-UNUSED-REGIONS)选项。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) | 包含要插入邮件合并字段的数据的行。字段名称不区分大小写。如果遇到在文档中找不到的字段名，则忽略它。 |

### execute(System.Data.DataTable table) {#execute-com.aspose.words.net.System.Data.DataTable-}
```
public void execute(System.Data.DataTable table)
```


执行从 com.aspose.words.net.System.Data.DataTable 到文档的邮件合并。

使用此方法用来自 a 的值填充文档中的邮件合并字段**DataTable**.

表中的所有记录都合并到文档中。

您可以使用 Word 文档中的 NEXT 字段来导致**MailMerge**对象从中选择下一条记录**DataTable**并继续合并。这可以在创建文档（例如邮寄标签）时使用。

什么时候**MailMerge**对象到达主文档的末尾并且还有更多的行在**DataTable**它复制主文档的全部内容并使用分节符作为分隔符将其附加到目标文档的末尾。

该方法忽略了[MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-UNUSED-REGIONS)选项。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable) | 包含要插入邮件合并字段的数据的表。字段名称不区分大小写。如果遇到在文档中找不到的字段名，则忽略它。 |

### execute(System.Data.DataView dataView) {#execute-com.aspose.words.net.System.Data.DataView-}
```
public void execute(System.Data.DataView dataView)
```


执行从 DataView 到文档的邮件合并。

如果您将数据检索到**DataTable**但随后需要在邮件合并之前应用过滤器或排序。

请注意，此方法不使用邮件合并区域，并且对于多个记录，文档将通过重复整个文档来增长。

该方法忽略了[MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-UNUSED-REGIONS)选项。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataView | [DataView](../../com.aspose.words.net.system.data/dataview) | 邮件合并操作的数据源。 |

### execute(System.Data.IDataReader dataReader) {#execute-com.aspose.words.net.System.Data.IDataReader-}
```
public void execute(System.Data.IDataReader dataReader)
```


执行从 IDataReader 到文档的邮件合并。

你可以通过**SqlDataReader**或者**OleDbDataReader**对象作为参数进入此方法，因为它们都实现了**IDataReader**界面。

请注意，此方法不使用邮件合并区域，并且对于多个记录，文档将通过重复整个文档来增长。

该方法忽略了[MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-UNUSED-REGIONS)选项。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataReader | [IDataReader](../../com.aspose.words.net.system.data/idatareader) | 邮件合并操作的数据源。 |

### execute(String[] fieldNames, Object[] values) {#execute-java.lang.String---java.lang.Object---}
```
public void execute(String[] fieldNames, Object[] values)
```


执行邮件合并操作。对单个记录执行邮件合并操作。

使用此方法用对象数组中的值填充文档中的邮件合并字段。

此方法仅合并一条记录的数据。字段名称数组和值数组表示单个记录的数据。

此方法不使用邮件合并区域。

该方法忽略了[MailMergeCleanupOptions.REMOVE\_UNUSED\_REGIONS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-UNUSED-REGIONS)选项。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fieldNames | java.lang.String[] | 合并字段名称数组。字段名称不区分大小写。如果遇到在文档中找不到的字段名，则忽略它。 |
| values | java.lang.Object[] | 要插入到合并字段中的值数组。此数组中的元素数必须与 fieldNames 中的元素数相同。 |

### executeWithRegions(IMailMergeDataSource dataSource) {#executeWithRegions-com.aspose.words.IMailMergeDataSource-}
```
public void executeWithRegions(IMailMergeDataSource dataSource)
```


从具有邮件合并区域的自定义数据源执行邮件合并。

使用此方法可以使用来自任何自定义数据源（例如 XML 文件或业务对象集合）的值填充文档中的邮件合并字段。您需要编写自己的类来实现[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource)界面。

您只能在以下情况下使用此方法[FieldOptions.isBidiTextSupportedOnUpdate()](../../com.aspose.words/fieldoptions\#isBidiTextSupportedOnUpdate--) / [FieldOptions.isBidiTextSupportedOnUpdate(boolean)](../../com.aspose.words/fieldoptions\#isBidiTextSupportedOnUpdate-boolean-)是假的，也就是说你不需要从右到左的语言（如阿拉伯语或希伯来语）兼容性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataSource | [IMailMergeDataSource](../../com.aspose.words/imailmergedatasource) | 实现自定义邮件合并数据源接口的对象。 |

### executeWithRegions(IMailMergeDataSourceRoot dataSourceRoot) {#executeWithRegions-com.aspose.words.IMailMergeDataSourceRoot-}
```
public void executeWithRegions(IMailMergeDataSourceRoot dataSourceRoot)
```


从具有邮件合并区域的自定义数据源执行邮件合并。

使用此方法可以使用来自任何自定义数据源（例如 XML 文件或业务对象集合）的值填充文档中的邮件合并字段。您需要编写自己的类来实现[IMailMergeDataSourceRoot](../../com.aspose.words/imailmergedatasourceroot)和[IMailMergeDataSource](../../com.aspose.words/imailmergedatasource)接口。

您只能在以下情况下使用此方法[FieldOptions.isBidiTextSupportedOnUpdate()](../../com.aspose.words/fieldoptions\#isBidiTextSupportedOnUpdate--) / [FieldOptions.isBidiTextSupportedOnUpdate(boolean)](../../com.aspose.words/fieldoptions\#isBidiTextSupportedOnUpdate-boolean-)是假的，也就是说你不需要从右到左的语言（如阿拉伯语或希伯来语）兼容性。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataSourceRoot | [IMailMergeDataSourceRoot](../../com.aspose.words/imailmergedatasourceroot) | 实现自定义邮件合并数据源根接口的对象。 |

### executeWithRegions(System.Data.DataSet dataSet) {#executeWithRegions-com.aspose.words.net.System.Data.DataSet-}
```
public void executeWithRegions(System.Data.DataSet dataSet)
```


对具有邮件合并区域的文档执行邮件合并操作。支持父子（主从）数据源和嵌套邮件合并区域。执行从 DataSet 到具有邮件合并区域的文档的邮件合并。

使用此方法将一个或多个表的邮件合并到文档中的可重复邮件合并区域。文档内的邮件合并区域将动态增长以容纳相应表中的记录。

文档必须具有使用引用数据集中表的名称定义的邮件合并区域。

要在文档中指定邮件合并区域，您需要插入两个邮件合并字段来标记邮件合并区域的开始和结束。

包含在邮件合并区域内的所有文档内容将针对 DataTable 中的每条记录自动重复。

要标记邮件合并区域的开始，请插入名称为 TableStart:MyTable 的 MERGEFIELD，其中 MyTable 对应于 DataSet 中的表名之一。

要标记邮件合并区域的结束，请插入另一个名称为 TableEnd:MyTable 的 MERGEFIELD。

要在 Word 中插入 MERGEFIELD，请使用 Insert/Field 命令并选择 MergeField，然后键入字段名称。

TableStart 和 TableEnd 字段必须在文档的同一部分内。

如果在表格内使用，TableStart 和 TableEnd 必须在表格的同一行内。

文档中的邮件合并区域应该格式正确（始终需要一对具有相同表名的匹配 TableStart 和 TableEnd 合并字段）。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataSet | [DataSet](../../com.aspose.words.net.system.data/dataset) | 包含要插入邮件合并字段的数据的数据集。 |

### executeWithRegions(System.Data.DataTable dataTable) {#executeWithRegions-com.aspose.words.net.System.Data.DataTable-}
```
public void executeWithRegions(System.Data.DataTable dataTable)
```


执行从 DataTable 到具有邮件合并区域的文档的邮件合并。

如果文档中定义了其他邮件合并区域，它们将保持原样。这允许执行多个邮件合并操作。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | 邮件合并操作的数据源。该表必须有其**TableName**属性集。 |

### executeWithRegions(System.Data.DataView dataView) {#executeWithRegions-com.aspose.words.net.System.Data.DataView-}
```
public void executeWithRegions(System.Data.DataView dataView)
```


执行从 DataView 到具有邮件合并区域的文档的邮件合并。

如果您将数据检索到**DataTable**但随后需要在邮件合并之前应用过滤器或排序。

该文档必须具有一个邮件合并区域，该区域定义的名称匹配**DataView.Table.TableName**.

如果文档中定义了其他邮件合并区域，它们将保持原样。这允许执行多个邮件合并操作。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataView | [DataView](../../com.aspose.words.net.system.data/dataview) | 邮件合并操作的数据源。的源表**DataView**必须有它的**TableName**属性集。 |

### executeWithRegions(System.Data.IDataReader dataReader, String tableName) {#executeWithRegions-com.aspose.words.net.System.Data.IDataReader-java.lang.String-}
```
public void executeWithRegions(System.Data.IDataReader dataReader, String tableName)
```


执行从 IDataReader 到具有邮件合并区域的文档的邮件合并。

你可以通过**SqlDataReader**或者**OleDbDataReader**对象作为参数进入此方法，因为它们都实现了**IDataReader**界面。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| dataReader | [IDataReader](../../com.aspose.words.net.system.data/idatareader) | 邮件合并的数据记录来源，例如 OleDbDataReader 或 SqlDataReader。 |
| tableName | java.lang.String | 文档中要填充的邮件合并区域的名称。 |

### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getCleanupOptions() {#getCleanupOptions--}
```
public int getCleanupOptions()
```


获取一组标志，这些标志指定在邮件合并期间应删除哪些项目。

**退货：**
 int - 一组标志，指定在邮件合并期间应删除哪些项目。返回值是按位组合[MailMergeCleanupOptions](../../com.aspose.words/mailmergecleanupoptions)常数。
### getCleanupParagraphsWithPunctuationMarks() {#getCleanupParagraphsWithPunctuationMarks--}
```
public boolean getCleanupParagraphsWithPunctuationMarks()
```


获取一个值，该值指示带有标点符号的段落是否被视为空，如果[MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-EMPTY-PARAGRAPHS)选项被指定。默认值是true 。以下是可清洁标点符号的完整列表：

 *  ！
 *  ,
 *  .
 *  :
 *  ;
 *  ？
 *  Ø
 *  Ø

**退货：**
 boolean - 一个值，指示带有标点符号的段落是否被视为空，如果[MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-EMPTY-PARAGRAPHS)选项被指定。
### getFieldMergingCallback() {#getFieldMergingCallback--}
```
public IFieldMergingCallback getFieldMergingCallback()
```


当在文档中遇到邮件合并字段时，在邮件合并期间发生。

**退货：**
[IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback) - 相应的[IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback)价值。
### getFieldNames() {#getFieldNames--}
```
public String[] getFieldNames()
```


返回文档中可用的邮件合并字段名称的集合。

返回包含可选前缀的完整合并字段名称。不会消除重复的字段名称。

一个新的字符串[数组在每次调用时创建。

包括“mustache”字段名称，如果[getUseNonMergeFields()](../../com.aspose.words/mailmerge\#getUseNonMergeFields--) / [setUseNonMergeFields(boolean)](../../com.aspose.words/mailmerge\#setUseNonMergeFields-boolean-)是**true**.

**退货：**
java.lang.字符串[]
### getFieldNamesForRegion(String regionName) {#getFieldNamesForRegion-java.lang.String-}
```
public String[] getFieldNamesForRegion(String regionName)
```


从区域获取邮件合并字段名称。返回区域中可用的邮件合并字段名称的集合。

返回包含可选前缀的完整合并字段名称。不会消除重复的字段名称。

如果文档包含多个同名区域，则处理第一个区域。

每次调用都会创建一个新的字符串数组。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| regionName | java.lang.String | 区域名称（不区分大小写）。 |

**退货：**
java.lang.字符串[]
### getFieldNamesForRegion(String regionName, int regionIndex) {#getFieldNamesForRegion-java.lang.String-int-}
```
public String[] getFieldNamesForRegion(String regionName, int regionIndex)
```


返回区域中可用的邮件合并字段名称的集合。

返回包含可选前缀的完整合并字段名称。不会消除重复的字段名称。

如果文档包含多个同名区域，则处理第 N 个区域（从零开始）。

每次调用都会创建一个新的字符串数组。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| regionName | java.lang.String | 区域名称（不区分大小写）。 |
| regionIndex | int | 区域索引（从零开始）。 |

**退货：**
java.lang.字符串[]
### getMailMergeCallback() {#getMailMergeCallback--}
```
public IMailMergeCallback getMailMergeCallback()
```


允许在邮件合并期间处理特定事件。

**退货：**
[IMailMergeCallback](../../com.aspose.words/imailmergecallback) - 相应的[IMailMergeCallback](../../com.aspose.words/imailmergecallback)价值。
### getMappedDataFields() {#getMappedDataFields--}
```
public MappedDataFieldCollection getMappedDataFields()
```


返回表示邮件合并操作的映射数据字段的集合。

映射数据字段允许在数据源中的字段名称和文档中邮件合并字段的名称之间自动映射。

**退货：**
[MappedDataFieldCollection](../../com.aspose.words/mappeddatafieldcollection) - 表示邮件合并操作的映射数据字段的集合。
### getMergeDuplicateRegions() {#getMergeDuplicateRegions--}
```
public boolean getMergeDuplicateRegions()
```


获取一个值，该值指示在针对数据源或仅第一个区域执行邮件合并时，是否应合并所有具有数据源名称的文档邮件合并区域。默认值为**false**.

**退货：**
boolean - 一个值，指示在针对数据源执行与区域的邮件合并时，是否应合并具有数据源名称的所有文档邮件合并区域，还是仅合并第一个。
### getMergeWholeDocument() {#getMergeWholeDocument--}
```
public boolean getMergeWholeDocument()
```


获取一个值，该值指示在执行区域邮件合并时是否更新整个文档中的字段。默认值为**false**.

**退货：**
boolean - 一个值，指示在执行与区域的邮件合并时是否更新整个文档中的字段。
### getPreserveUnusedTags() {#getPreserveUnusedTags--}
```
public boolean getPreserveUnusedTags()
```


获取一个值，该值指示是否应保留未使用的“小胡子”标签。默认值为**false**.

**退货：**
boolean - 一个值，指示是否应保留未使用的“mustache”标签。
### getRegionEndTag() {#getRegionEndTag--}
```
public String getRegionEndTag()
```


获取邮件合并区域结束标记。

**退货：**
java.lang.String - 邮件合并区域结束标记。
### getRegionStartTag() {#getRegionStartTag--}
```
public String getRegionStartTag()
```


获取邮件合并区域开始标记。

**退货：**
java.lang.String - 邮件合并区域开始标记。
### getRegionsByName(String regionName) {#getRegionsByName-java.lang.String-}
```
public ArrayList getRegionsByName(String regionName)
```


返回具有指定名称的邮件合并区域的集合。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| regionName | java.lang.String | 区域名称（不区分大小写）。 |

**退货：**
java.util.ArrayList - 区域列表。
### getRegionsHierarchy() {#getRegionsHierarchy--}
```
public MailMergeRegionInfo getRegionsHierarchy()
```


返回文档中可用区域（带有字段）的完整层次结构。

层次结构以[MailMergeRegionInfo](../../com.aspose.words/mailmergeregioninfo)班级。

**退货：**
[MailMergeRegionInfo](../../com.aspose.words/mailmergeregioninfo) 地区的层次结构。
### getRestartListsAtEachSection() {#getRestartListsAtEachSection--}
```
public boolean getRestartListsAtEachSection()
```


获取一个值，该值指示在执行邮件合并后是否在每个部分重新启动列表。默认值为**true**.

**退货：**
boolean - 一个值，表示在执行邮件合并后列表是否在每个部分重新启动。
### getRetainFirstSectionStart() {#getRetainFirstSectionStart--}
```
public boolean getRetainFirstSectionStart()
```


获取一个值，该值指示是否[PageSetup.getSectionStart()](../../com.aspose.words/pagesetup\#getSectionStart--) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup\#setSectionStart-int-)第一个文档部分及其后续数据源行的副本在邮件合并期间保留或根据 MS Word 行为更新。默认值为**true**.

**退货：**
布尔值 - 一个值，指示是否[PageSetup.getSectionStart()](../../com.aspose.words/pagesetup\#getSectionStart--) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup\#setSectionStart-int-)第一个文档部分及其后续数据源行的副本在邮件合并期间保留或根据 MS Word 行为更新。
### getTrimWhitespaces() {#getTrimWhitespaces--}
```
public boolean getTrimWhitespaces()
```


获取一个值，该值指示是否从邮件合并值中删除尾随和前导空格。默认值为**true**.

**退货：**
boolean - 一个值，指示是否从邮件合并值中删除尾随和前导空格。
### getUnconditionalMergeFieldsAndRegions() {#getUnconditionalMergeFieldsAndRegions--}
```
public boolean getUnconditionalMergeFieldsAndRegions()
```


获取一个值，该值指示是否合并合并字段和合并区域，而不管父 IF 字段的条件如何。默认值为**false**.

**退货：**
布尔值 - 一个值，指示是否合并合并字段和合并区域，而不管父 IF 字段的条件如何。
### getUseNonMergeFields() {#getUseNonMergeFields--}
```
public boolean getUseNonMergeFields()
```


当为 true 时，指定除了 MERGEFIELD 字段之外，邮件合并被执行到一些其他类型的字段中，也被执行到“\{\{字段名\}\}”标签。

通常，邮件合并仅在 MERGEFIELD 字段中执行，但一些客户使用其他字段构建了他们的报告，并以这种方式创建了许多文档。为了简化迁移（并且因为这种方法被多个客户独立使用），引入了将邮件合并到其他字段的能力。

什么时候**UseNonMergeFields**设置为true，Aspose.Words将执行邮件合并到以下字段：

MERGEFIELD 字段名

MACROBUTTON NOMACRO 字段名

如果 0 = 0"\{字段名\}" ""

还有，当**UserNonMergeFields**设置为true，Aspose.Words会执行邮件合并到文本标签中”\{\{字段名\}\}”。这些不是字段，而只是文本标签。

**退货：**
boolean - 相应的布尔值。
### getUseWholeParagraphAsRegion() {#getUseWholeParagraphAsRegion--}
```
public boolean getUseWholeParagraphAsRegion()
```


获取一个值，该值指示是否应将具有 TableStart 或 TableEnd 字段的整个段落或 TableStart 和 TableEnd 字段之间的特定范围包含到邮件合并区域中。默认值为**true**.

**退货：**
boolean - 一个值，指示是否应将具有 TableStart 或 TableEnd 字段的整个段落或 TableStart 和 TableEnd 字段之间的特定范围包含到邮件合并区域中。
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




### setCleanupOptions(int value) {#setCleanupOptions-int-}
```
public void setCleanupOptions(int value)
```


设置一组标志，指定在邮件合并期间应删除哪些项目。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 一组标志，指定在邮件合并期间应删除哪些项目。该值必须是按位组合[MailMergeCleanupOptions](../../com.aspose.words/mailmergecleanupoptions)常数。 |

### setCleanupParagraphsWithPunctuationMarks(boolean value) {#setCleanupParagraphsWithPunctuationMarks-boolean-}
```
public void setCleanupParagraphsWithPunctuationMarks(boolean value)
```


设置一个值，指示带标点符号的段落是否被视为空的，如果[MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-EMPTY-PARAGRAPHS)选项被指定。默认值是true 。以下是可清洁标点符号的完整列表：

 *  ！
 *  ,
 *  .
 *  :
 *  ;
 *  ？
 *  Ø
 *  Ø

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，指示带标点符号的段落是否被视为空的，如果[MailMergeCleanupOptions.REMOVE\_EMPTY\_PARAGRAPHS](../../com.aspose.words/mailmergecleanupoptions\#REMOVE-EMPTY-PARAGRAPHS)选项被指定。 |

### setFieldMergingCallback(IFieldMergingCallback value) {#setFieldMergingCallback-com.aspose.words.IFieldMergingCallback-}
```
public void setFieldMergingCallback(IFieldMergingCallback value)
```


当在文档中遇到邮件合并字段时，在邮件合并期间发生。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback) | 相应的[IFieldMergingCallback](../../com.aspose.words/ifieldmergingcallback)价值。 |

### setMailMergeCallback(IMailMergeCallback value) {#setMailMergeCallback-com.aspose.words.IMailMergeCallback-}
```
public void setMailMergeCallback(IMailMergeCallback value)
```


允许在邮件合并期间处理特定事件。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [IMailMergeCallback](../../com.aspose.words/imailmergecallback) | 相应的[IMailMergeCallback](../../com.aspose.words/imailmergecallback)价值。 |

### setMergeDuplicateRegions(boolean value) {#setMergeDuplicateRegions-boolean-}
```
public void setMergeDuplicateRegions(boolean value)
```


设置一个值，该值指示在针对数据源或仅第一个区域执行邮件合并时，是否应合并所有具有数据源名称的文档邮件合并区域。默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，指示在针对数据源或仅第一个区域执行邮件合并时，是否应合并所有具有数据源名称的文档邮件合并区域。 |

### setMergeWholeDocument(boolean value) {#setMergeWholeDocument-boolean-}
```
public void setMergeWholeDocument(boolean value)
```


设置一个值，指示在执行与区域的邮件合并时是否更新整个文档中的字段。默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，指示在执行与区域的邮件合并时是否更新整个文档中的字段。 |

### setPreserveUnusedTags(boolean value) {#setPreserveUnusedTags-boolean-}
```
public void setPreserveUnusedTags(boolean value)
```


设置一个值，指示是否应保留未使用的“小胡子”标签。默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否应保留未使用的“小胡子”标签的值。 |

### setRegionEndTag(String value) {#setRegionEndTag-java.lang.String-}
```
public void setRegionEndTag(String value)
```


设置邮件合并区域结束标记。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 邮件合并区域结束标记。 |

### setRegionStartTag(String value) {#setRegionStartTag-java.lang.String-}
```
public void setRegionStartTag(String value)
```


设置邮件合并区域开始标记。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 邮件合并区域开始标记。 |

### setRestartListsAtEachSection(boolean value) {#setRestartListsAtEachSection-boolean-}
```
public void setRestartListsAtEachSection(boolean value)
```


设置一个值，该值指示在执行邮件合并后是否在每个部分重新启动列表。默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，表示在执行邮件合并后是否在每个部分重新启动列表。 |

### setRetainFirstSectionStart(boolean value) {#setRetainFirstSectionStart-boolean-}
```
public void setRetainFirstSectionStart(boolean value)
```


设置一个值，指示是否[PageSetup.getSectionStart()](../../com.aspose.words/pagesetup\#getSectionStart--) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup\#setSectionStart-int-)第一个文档部分及其后续数据源行的副本在邮件合并期间保留或根据 MS Word 行为更新。默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值指示是否[PageSetup.getSectionStart()](../../com.aspose.words/pagesetup\#getSectionStart--) / [PageSetup.setSectionStart(int)](../../com.aspose.words/pagesetup\#setSectionStart-int-)第一个文档部分及其后续数据源行的副本在邮件合并期间保留或根据 MS Word 行为更新。 |

### setTrimWhitespaces(boolean value) {#setTrimWhitespaces-boolean-}
```
public void setTrimWhitespaces(boolean value)
```


设置一个值，该值指示是否从邮件合并值中删除尾随和前导空格。默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，指示是否从邮件合并值中删除尾随和前导空格。 |

### setUnconditionalMergeFieldsAndRegions(boolean value) {#setUnconditionalMergeFieldsAndRegions-boolean-}
```
public void setUnconditionalMergeFieldsAndRegions(boolean value)
```


设置一个值，指示是否合并合并字段和合并区域，而不管父 IF 字段的条件如何。默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，指示是否合并合并字段和合并区域，而不管父 IF 字段的条件如何。 |

### setUseNonMergeFields(boolean value) {#setUseNonMergeFields-boolean-}
```
public void setUseNonMergeFields(boolean value)
```


当为 true 时，指定除了 MERGEFIELD 字段之外，邮件合并被执行到一些其他类型的字段中，也被执行到“\{\{字段名\}\}”标签。

通常，邮件合并仅在 MERGEFIELD 字段中执行，但一些客户使用其他字段构建了他们的报告，并以这种方式创建了许多文档。为了简化迁移（并且因为这种方法被多个客户独立使用），引入了将邮件合并到其他字段的能力。

什么时候**UseNonMergeFields**设置为true，Aspose.Words将执行邮件合并到以下字段：

MERGEFIELD 字段名

MACROBUTTON NOMACRO 字段名

如果 0 = 0"\{字段名\}" ""

还有，当**UserNonMergeFields**设置为true，Aspose.Words会执行邮件合并到文本标签中”\{\{字段名\}\}”。这些不是字段，而只是文本标签。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setUseWholeParagraphAsRegion(boolean value) {#setUseWholeParagraphAsRegion-boolean-}
```
public void setUseWholeParagraphAsRegion(boolean value)
```


设置一个值，指示是否应将具有 TableStart 或 TableEnd 字段的整个段落或 TableStart 和 TableEnd 字段之间的特定范围包含到邮件合并区域中。默认值为**true**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，指示是否应将具有 TableStart 或 TableEnd 字段的整个段落或 TableStart 和 TableEnd 字段之间的特定范围包含到邮件合并区域中。 |

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
