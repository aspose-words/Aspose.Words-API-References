---
title: MailMergeSettings.CheckErrors
linktitle: CheckErrors
articleTitle: CheckErrors
second_title: Aspose.Words for .NET
description: 探索 Microsoft Word 中的 MailMergeSettings CheckErrors 属性，以便在邮件合并期间有效地报告错误。立即优化您的工作流程！
type: docs
weight: 40
url: /zh/net/aspose.words.settings/mailmergesettings/checkerrors/
---
## MailMergeSettings.CheckErrors property

指定 Microsoft Word 在执行邮件合并时应进行的错误报告类型。 默认值为Default.

```csharp
public MailMergeCheckErrors CheckErrors { get; set; }
```

## 例子

展示如何使用来自 Office 数据源对象的数据执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// 以ASCII文件的形式创建数据源，以“|”字符
// 充当分隔列的分隔符。第一行包含三列的名称，
// 并且每个后续行都是具有各自值的一行。
string[] lines = { "FirstName|LastName|Message",
    "John|Doe|Hello! This message was created with Aspose Words mail merge." };
string dataSrcFilename = ArtifactsDir + "MailMerge.MailMergeSettings.DataSource.txt";

File.WriteAllLines(dataSrcFilename, lines);

MailMergeSettings settings = doc.MailMergeSettings;
settings.MainDocumentType = MailMergeMainDocumentType.MailingLabels;
settings.CheckErrors = MailMergeCheckErrors.Simulate;
settings.DataType = MailMergeDataType.Native;
settings.DataSource = dataSrcFilename;
settings.Query = "SELECT * FROM " + doc.MailMergeSettings.DataSource;
settings.LinkToQuery = true;
settings.ViewMergedData = true;

Assert.AreEqual(MailMergeDestination.Default, settings.Destination);
Assert.False(settings.DoNotSupressBlankLines);

Odso odso = settings.Odso;
odso.DataSource = dataSrcFilename;
odso.DataSourceType = OdsoDataSourceType.Text;
odso.ColumnDelimiter = '|';
odso.FirstRowContainsColumnNames = true;

Assert.AreNotSame(odso, odso.Clone());
Assert.AreNotSame(settings, settings.Clone());

 // 在 Microsoft Word 中打开此文档将在显示内容之前执行邮件合并。
doc.Save(ArtifactsDir + "MailMerge.MailMergeSettings.docx");
```

### 也可以看看

* enum [MailMergeCheckErrors](../../mailmergecheckerrors/)
* class [MailMergeSettings](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
