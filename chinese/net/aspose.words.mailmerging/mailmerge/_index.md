---
title: MailMerge
second_title: Aspose.Words for .NET API 参考
description: 表示邮件合并功能
type: docs
weight: 3570
url: /zh/net/aspose.words.mailmerging/mailmerge/
---
## MailMerge class

表示邮件合并功能。

```csharp
public class MailMerge
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CleanupOptions](../../aspose.words.mailmerging/mailmerge/cleanupoptions) { get; set; } | 获取或设置一组标志，这些标志指定在邮件合并期间应删除哪些项目。 |
| [CleanupParagraphsWithPunctuationMarks](../../aspose.words.mailmerging/mailmerge/cleanupparagraphswithpunctuationmarks) { get; set; } | 获取或设置一个值，该值指示是否将带有标点符号的段落视为空 并且如果RemoveEmptyParagraphs选项被指定。 |
| [FieldMergingCallback](../../aspose.words.mailmerging/mailmerge/fieldmergingcallback) { get; set; } | 在文档中遇到邮件合并字段时在邮件合并期间发生。 |
| [MailMergeCallback](../../aspose.words.mailmerging/mailmerge/mailmergecallback) { get; set; } | 允许在邮件合并期间处理特定事件。 |
| [MappedDataFields](../../aspose.words.mailmerging/mailmerge/mappeddatafields) { get; } | 返回代表邮件合并操作的映射数据字段的集合。 |
| [MergeDuplicateRegions](../../aspose.words.mailmerging/mailmerge/mergeduplicateregions) { get; set; } | 获取或设置一个值，该值指示在执行邮件与数据源或仅第一个区域合并。 |
| [MergeWholeDocument](../../aspose.words.mailmerging/mailmerge/mergewholedocument) { get; set; } | 获取或设置一个值，该值指示在执行与区域的邮件合并时是否更新整个文档中的字段。 |
| [PreserveUnusedTags](../../aspose.words.mailmerging/mailmerge/preserveunusedtags) { get; set; } | 获取或设置一个值，该值指示是否应保留未使用的“mustache”标签。 |
| [RegionEndTag](../../aspose.words.mailmerging/mailmerge/regionendtag) { get; set; } | 获取或设置邮件合并区域结束标记。 |
| [RegionStartTag](../../aspose.words.mailmerging/mailmerge/regionstarttag) { get; set; } | 获取或设置邮件合并区域开始标记。 |
| [RestartListsAtEachSection](../../aspose.words.mailmerging/mailmerge/restartlistsateachsection) { get; set; } | 获取或设置一个值，该值指示在执行邮件合并后是否在每个部分重新启动列表。 |
| [RetainFirstSectionStart](../../aspose.words.mailmerging/mailmerge/retainfirstsectionstart) { get; set; } | 获取或设置一个值，该值指示第一个文档节的[`SectionStart`](../../aspose.words/pagesetup/sectionstart)及其副本是否用于后续数据源行 在邮件合并期间保留或根据 MS Word 行为进行更新。 |
| [TrimWhitespaces](../../aspose.words.mailmerging/mailmerge/trimwhitespaces) { get; set; } | 获取或设置一个值，该值指示是否从邮件合并值中修剪尾随和前导空格。 |
| [UnconditionalMergeFieldsAndRegions](../../aspose.words.mailmerging/mailmerge/unconditionalmergefieldsandregions) { get; set; } | 获取或设置一个值，该值指示是否合并合并字段和合并区域，而不考虑父 IF 字段的条件。 |
| [UseNonMergeFields](../../aspose.words.mailmerging/mailmerge/usenonmergefields) { get; set; } | 当为 true 时，指定除了 MERGEFIELD 字段之外，邮件合并到一些其他类型的字段和 也到 "{{fieldName }}”标签。 |
| [UseWholeParagraphAsRegion](../../aspose.words.mailmerging/mailmerge/usewholeparagraphasregion) { get; set; } | 获取或设置一个值，该值指示是否应将具有 TableStart 或 TableEnd 字段 或 TableStart 和 TableEnd 字段之间的特定范围的整个段落包含到邮件合并中地区。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [DeleteFields](../../aspose.words.mailmerging/mailmerge/deletefields)() | 从文档中删除邮件合并相关字段。 |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_1)(DataRow) | 执行从 DataRow 到文档的邮件合并。 |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_2)(DataTable) | 将数据表中的邮件合并到文档中。 |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_3)(DataView) | 执行从 DataView 到文档的邮件合并。 |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_4)(IDataReader) | 将邮件从 IDataReader 合并到文档中。 |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute)(IMailMergeDataSource) | 从自定义数据源执行邮件合并。 |
| [Execute](../../aspose.words.mailmerging/mailmerge/execute#execute_5)(string[], object[]) | 对单个记录执行邮件合并操作。 |
| [ExecuteADO](../../aspose.words.mailmerging/mailmerge/executeado)(object) | 执行从 ADO Recordset 对象到文档的邮件合并。 |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_2)(DataSet) | 将数据集的邮件合并到具有邮件合并区域的文档中。 |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_3)(DataTable) | 将数据表中的邮件合并到带有邮件合并区域的文档中。 |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_4)(DataView) | 执行从 DataView 到具有邮件合并区域的文档的邮件合并。 |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions)(IMailMergeDataSource) | 从具有邮件合并区域的自定义数据源执行邮件合并。 |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_1)(IMailMergeDataSourceRoot) | 从具有邮件合并区域的自定义数据源执行邮件合并。 |
| [ExecuteWithRegions](../../aspose.words.mailmerging/mailmerge/executewithregions#executewithregions_5)(IDataReader, string) | 执行从 IDataReader 到具有邮件合并区域的文档的邮件合并。 |
| [ExecuteWithRegionsADO](../../aspose.words.mailmerging/mailmerge/executewithregionsado)(object, string) | 执行从 ADO Recordset 对象到具有邮件合并区域的文档的邮件合并。 |
| [GetFieldNames](../../aspose.words.mailmerging/mailmerge/getfieldnames)() | 返回文档中可用的邮件合并字段名称的集合。 |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion#getfieldnamesforregion)(string) | 返回区域中可用的邮件合并字段名称的集合。 |
| [GetFieldNamesForRegion](../../aspose.words.mailmerging/mailmerge/getfieldnamesforregion#getfieldnamesforregion_1)(string, int) | 返回区域中可用的邮件合并字段名称的集合。 |
| [GetRegionsByName](../../aspose.words.mailmerging/mailmerge/getregionsbyname)(string) | 返回具有指定名称的邮件合并区域的集合。 |
| [GetRegionsHierarchy](../../aspose.words.mailmerging/mailmerge/getregionshierarchy)() | 返回文档中可用区域（带有字段）的完整层次结构。 |

### 评论

要使邮件合并操作生效，文档应包含 Word MERGEFIELD 和 可选的 NEXT 字段。在邮件合并操作期间，文档中的合并字段被 替换为您的数据源中的值。

使用邮件合并有两种不同的方式:使用邮件合并区域和不使用邮件合并区域。

最简单的邮件合并是没有区域的，它与邮件合并 在 Word 中的工作方式非常相似。使用 执行 方法来合并来自一些 数据源的信息，例如 **DataTable** , **DataSet** , **DataView** , **IDataReader** 或一个对象数组到您的文档中。  **MailMerge** 对象处理数据源的所有记录并复制和附加整个文档的 内容以用于每条记录。

请注意，当 **MailMerge** 对象遇到 NEXT 字段时，它会选择下一条记录 在数据源中并继续合并而不复制任何内容。

使用 ExecuteWithRegions 方法将信息合并到带有邮件的 文档中合并区域定义。您可以使用  **DataSet** , **DataTable** , **DataView** 或 **IDataReader** 作为此操作的数据源。

如果要在 文档中动态增长部分，则需要使用邮件合并区域。如果没有邮件合并区域，整个文档将针对 数据源的每条记录重复。

### 例子

显示如何使用 DataTable 中的数据执行邮件合并。

```csharp
public void ExecuteDataTable()
{
    DataTable table = new DataTable("Test");
    table.Columns.Add("CustomerName");
    table.Columns.Add("Address");
    table.Rows.Add(new object[] { "Thomas Hardy", "120 Hanover Sq., London" });
    table.Rows.Add(new object[] { "Paolo Accorti", "Via Monte Bianco 34, Torino" });

     // 下面是使用DataTable作为邮件合并数据源的两种方式。
    // 1 - 使用整个表进行邮件合并，为表中的每一行创建一个输出邮件合并文档：
    Document doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.WholeTable.docx");

     // 2 - 使用表格的一行创建一个输出邮件合并文档：
    doc = CreateSourceDocExecuteDataTable();

    doc.MailMerge.Execute(table.Rows[1]);

    doc.Save(ArtifactsDir + "MailMerge.ExecuteDataTable.OneRow.docx");
}

/// <summary>
 /// 创建一个邮件合并源文档。
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

* namespace [Aspose.Words.MailMerging](../../aspose.words.mailmerging)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
