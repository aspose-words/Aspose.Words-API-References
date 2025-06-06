---
title: MailMergeSettings.HeaderSource
linktitle: HeaderSource
articleTitle: HeaderSource
second_title: Aspose.Words for .NET
description: 探索 MailMergeSettings HeaderSource 属性，轻松定义邮件合并标头路径。立即优化您的文档工作流程！
type: docs
weight: 100
url: /zh/net/aspose.words.settings/mailmergesettings/headersource/
---
## MailMergeSettings.HeaderSource property

指定邮件合并标头源的路径。 默认值为空字符串。

```csharp
public string HeaderSource { get; set; }
```

## 例子

展示如何从标题源和数据源构建邮件合并的数据源。

```csharp
// 创建一个邮件标签合并头文件，该文件将由一个包含一行的表组成。
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("FirstName");
builder.InsertCell();
builder.Write("LastName");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx");

// 创建一个由一行表格组成的邮件标签合并数据文件
// 并且与标题文档的表格具有相同数量的列。
doc = new Document();
builder = new DocumentBuilder(doc);

builder.StartTable();
builder.InsertCell();
builder.Write("John");
builder.InsertCell();
builder.Write("Doe");
builder.EndTable();

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx");

// 使用 MERGEFIELDS 创建一个合并目标文档，其名称为
// 匹配合并头文件表中的列名。
doc = new Document();
builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");

MailMergeSettings settings = doc.MailMergeSettings;

// 通过指定两个文档文件名来构建我们的邮件合并的数据源。
// 标题源将命名数据源表的列。
settings.HeaderSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Header.docx";

// 数据源将为标题文档表中的所有列提供数据行。
settings.DataSource = ArtifactsDir + "MailMerge.MailingLabelMerge.Data.docx";

// 配置邮件标签类型邮件合并，Microsoft Word 将执行
// 一旦我们使用它来加载输出文档。
settings.Query = "SELECT * FROM " + settings.DataSource;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.DataType = MailMergeDataType.TextFile;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

doc.Save(ArtifactsDir + "MailMerge.MailingLabelMerge.docx");
```

### 也可以看看

* class [MailMergeSettings](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
