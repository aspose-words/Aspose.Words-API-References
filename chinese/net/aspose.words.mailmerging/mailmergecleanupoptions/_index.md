---
title: MailMergeCleanupOptions Enum
linktitle: MailMergeCleanupOptions
articleTitle: MailMergeCleanupOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.MailMergeCleanupOptions 枚举，高效管理邮件合并清理。通过无缝控制项目删除，优化您的文档。
type: docs
weight: 4540
url: /zh/net/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enumeration

指定确定邮件合并期间删除哪些项目的选项。

```csharp
[Flags]
public enum MailMergeCleanupOptions
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 指定默认值。 |
| RemoveEmptyParagraphs | `1` | 指定是否应从文档中删除包含没有数据的邮件合并字段的段落。 设置此选项后，包含区域开始和结束合并字段（否则为空）的段落也将被删除。 |
| RemoveUnusedRegions | `2` | 指定是否应从文档中删除未使用的邮件合并区域。 |
| RemoveUnusedFields | `4` | 指定是否应从文档中删除未使用的合并字段。 |
| RemoveContainingFields | `8` | 指定是否应从文档中删除包含合并字段（例如，IF）的字段 （如果嵌套的合并字段被删除）。 |
| RemoveStaticFields | `10` | 指定是否应从文档中移除静态字段。静态字段是指其结果在任何文档更改后保持不变的字段。 则是指不将结果存储在文档中且会动态计算的字段（例如FieldListNum , FieldSymbol等）不被视为静态的。 |
| RemoveEmptyTableRows | `20` | 指定是否应从文档中删除包含邮件合并区域的空行。 |
| RemoveEmptyTables | `40` | 指定是否从包含已使用 删除的邮件合并区域的文档表中删除RemoveUnusedRegions或RemoveEmptyTableRows选项. |

## 例子

显示如何在邮件合并期间删除整个空表。

```csharp
DataTable tableCustomers = new DataTable("A");
tableCustomers.Columns.Add("CustomerID");
tableCustomers.Columns.Add("CustomerName");
tableCustomers.Rows.Add(new object[] { 1, "John Doe" });
tableCustomers.Rows.Add(new object[] { 2, "Jane Doe" });

DataSet ds = new DataSet();
ds.Tables.Add(tableCustomers);

Document doc = new Document(MyDir + "Mail merge tables.docx");
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

doc.MailMerge.MergeDuplicateRegions = false;
doc.MailMerge.CleanupOptions = MailMergeCleanupOptions.RemoveEmptyTables | MailMergeCleanupOptions.RemoveUnusedRegions;
doc.MailMerge.ExecuteWithRegions(ds.Tables["A"]);

doc.Save(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");

doc = new Document(ArtifactsDir + "MailMerge.RemoveEmptyTables.docx");
Assert.AreEqual(1, doc.GetChildNodes(NodeType.Table, true).Count);
```

展示如何从合并输出文档中删除邮件合并可能创建的空段落。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertField(" MERGEFIELD TableStart:MyTable");
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertField(" MERGEFIELD TableEnd:MyTable");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "", "" });
dataTable.Rows.Add(new object[] { "Jane", "Doe" });

doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.ExecuteWithRegions(dataTable);

if (doc.MailMerge.CleanupOptions == MailMergeCleanupOptions.RemoveEmptyParagraphs) 
    Assert.AreEqual(
        "John Doe\r" +
        "Jane Doe", doc.GetText().Trim());
else
    Assert.AreEqual(
        "John Doe\r" +
        " \r" +
        "Jane Doe", doc.GetText().Trim());
```

显示如何自动删除邮件合并期间未使用的 MERGEFIELD。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 创建一个包含邮件合并数据源表三列的 MERGEFIELDs 文档，
// 然后创建一个只有两列且其名称与我们的 MERGEFIELDs 匹配的表。
builder.InsertField(" MERGEFIELD FirstName ");
builder.Write(" ");
builder.InsertField(" MERGEFIELD LastName ");
builder.InsertParagraph();
builder.InsertField(" MERGEFIELD City ");

DataTable dataTable = new DataTable("MyTable");
dataTable.Columns.Add("FirstName");
dataTable.Columns.Add("LastName");
dataTable.Rows.Add(new object[] { "John", "Doe" });
dataTable.Rows.Add(new object[] { "Joe", "Bloggs" });

// 我们的第三个 MERGEFIELD 引用了“城市”列，但该列在我们的数据源中不存在。
// 邮件合并将使此类字段保持合并前的状态不变。
// 将“CleanupOptions”属性设置为“RemoveUnusedFields”将删除任何 MERGEFIELDs
// 在邮件合并期间未使用以清理合并文档。
doc.MailMerge.CleanupOptions = mailMergeCleanupOptions;
doc.MailMerge.Execute(dataTable);

if (mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveUnusedFields || 
    mailMergeCleanupOptions == MailMergeCleanupOptions.RemoveStaticFields)
    Assert.AreEqual(0, doc.Range.Fields.Count);
else
    Assert.AreEqual(2, doc.Range.Fields.Count);
```

### 也可以看看

* 命名空间 [Aspose.Words.MailMerging](../../aspose.words.mailmerging/)
* 部件 [Aspose.Words](../../)
