---
title: Class MailMerge
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.MailMerging.MailMerge 班级. 代表邮件合并功能
type: docs
weight: 3840
url: /zh/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

代表邮件合并功能。

要了解更多信息，请访问[邮件合并和报告](https://docs.aspose.com/words/net/mail-merge-and-reporting/)文档文章。

```csharp
public class MailMerge
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions/) { get; set; } | 获取或设置一组标志，指定在邮件合并期间应删除哪些项目。 |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks/) { get; set; } | 获取或设置一个值，该值指示带标点符号的段落是否被视为空 ，并且如果RemoveEmptyParagraphs已指定选项。 |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback/) { get; set; } | 在邮件合并过程中，当文档中遇到邮件合并字段时发生。 |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback/) { get; set; } | 允许在邮件合并期间处理特定事件。 |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields/) { get; } | 返回表示邮件合并操作的映射数据字段的集合。 |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions/) { get; set; } | 获取或设置一个值，该值指示在针对数据源或仅第一个区域执行邮件合并时是否应合并具有数据源 名称的所有文档邮件合并区域。 |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument/) { get; set; } | 获取或设置一个值，该值指示在执行区域邮件合并时是否更新整个文档中的字段。 |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags/) { get; set; } | 获取或设置一个值，该值指示是否应保留未使用的“mustache”标签。 |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag/) { get; set; } | 获取或设置邮件合并区域结束标记。 |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag/) { get; set; } | 获取或设置邮件合并区域开始标记。 |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection/) { get; set; } | 获取或设置一个值，该值指示执行邮件合并后是否在每个部分重新启动列表。 |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart/) { get; set; } | 获取或设置一个值，指示是否[`SectionStart`](../../aspose.words/pagesetup/sectionstart/)第一个文档部分及其后续数据源行的副本 在邮件合并期间保留或根据 MS Word 行为进行更新。 |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces/) { get; set; } | 获取或设置一个值，该值指示是否从邮件合并值中删除尾随和前导空格。 |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions/) { get; set; } | 获取或设置一个值，该值指示合并字段和合并区域是否合并，无论父 IF 字段的条件如何。 |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields/) { get; set; } | 当`真的`，指定除了 MERGEFIELD 字段之外，还会将邮件合并到其他一些类型的字段中，并且 还执行到“{{fieldName}}”标签中。 |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion/) { get; set; } | 获取或设置一个值，指示整个段落是否包含 **开始表**或者 **桌尾**field 或之间的特定范围 **开始表**和 **桌尾**字段应包含在邮件合并区域中。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields/)() | 从文档中删除邮件合并相关字段。 |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_1)(DataRow) | 从 a 执行邮件合并 **数据行**进入文档. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_2)(DataTable) | 将数据表中的邮件合并到文档中。 |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_3)(DataView) | 从 a 执行邮件合并 **数据视图**进入文档. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_4)(IDataReader) | 执行邮件合并 **数据读取器**进入文档. |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute)(IMailMergeDataSource) | 从自定义数据源执行邮件合并。 |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute/#execute_5)(string[], object[]) | 对单个记录执行邮件合并操作。 |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado/)(object) | 将 ADO Recordset 对象的邮件合并到文档中。 |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_2)(DataSet) | 从 a 执行邮件合并 **数据集**到具有邮件合并区域的文档中。 |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_3)(DataTable) | 从 a 执行邮件合并 **数据表**进入带有邮件合并区域的文档。 |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_4)(DataView) | 从 a 执行邮件合并 **数据视图**进入带有邮件合并区域的文档。 |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions)(IMailMergeDataSource) | 从具有邮件合并区域的自定义数据源执行邮件合并。 |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_1)(IMailMergeDataSourceRoot) | 从具有邮件合并区域的自定义数据源执行邮件合并。 |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions/#executewithregions_5)(IDataReader, string) | 执行邮件合并 **数据读取器**进入带有邮件合并区域的文档。 |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado/)(object, string) | 将 ADO Recordset 对象的邮件合并到具有邮件合并区域的文档中。 |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames/)() | 返回文档中可用的邮件合并字段名称的集合。 |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion)(string) | 返回该区域中可用的邮件合并字段名称的集合。 |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion/#getfieldnamesforregion_1)(string, int) | 返回该区域中可用的邮件合并字段名称的集合。 |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname/)(string) | 返回具有指定名称的邮件合并区域的集合。 |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy/)() | 返回文档中可用区域（带字段）的完整层次结构。 |

### 评论

为了使邮件合并操作正常工作，文档应包含 Word MERGEFIELD 和 （可选）NEXT 字段。在邮件合并操作期间，文档中的合并字段 are 替换为数据源中的值。

使用邮件合并有两种不同的方式：使用邮件合并区域和不使用邮件合并区域。

最简单的邮件合并是没有区域的，它与 Word 中邮件 merge 的工作方式非常相似。使用执行合并来自 some 数据源的信息的方法，例如 **数据表**, **数据集**, **数据视图**, **数据读取器** 或对象数组到您的文档中。 The `MailMerge`对象处理数据源的所有记录，并为每条记录复制并追加整个文档的 内容。

请注意，当`MailMerge`对象遇到 NEXT 字段，它会选择数据源中的下一个 record 并继续合并，而不复制任何内容。

使用[`ExecuteWithRegions`](./executewithregions/)和其他重载，将信息合并到定义了邮件合并区域的 a 文档中。您可以使用  **数据集**, **数据表**, **数据视图**或者 **数据读取器** 作为此操作的数据源。

如果您想动态增长 the 文档中的部分，则需要使用邮件合并区域。如果没有邮件合并区域，整个文档将针对数据源 的每条记录重复。

### 例子

演示如何使用数据表中的数据执行邮件合并。

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

    // 下面是使用 DataTable 作为邮件合并数据源的两种方法。
    // 1 - 使用整个表进行邮件合并，为表中的每一行创建一个输出邮件合并文档：
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

    // 2 - 使用表的一行创建一个输出邮件合并文档：
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
/// 创建邮件合并源文档。
/// </summary>
private static Document CreateSourceDocExecuteDataTable()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.InsertField(" MERGEFIELD CustomerName ");
    builder.InsertParagraph();
    builder.InsertField(" MERGEFIELD Address ");

    return doc;
}
```

### 也可以看看

* 命名空间 [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../)


