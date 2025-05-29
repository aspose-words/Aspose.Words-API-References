---
title: MailMergeSettings.MainDocumentType
linktitle: MainDocumentType
articleTitle: MainDocumentType
second_title: Aspose.Words for .NET
description: 了解 MailMergeSettings 的 MainDocumentType 属性如何定义您的邮件合并文档。通过最佳设置，轻松创建无缝文档！
type: docs
weight: 140
url: /zh/net/aspose.words.settings/mailmergesettings/maindocumenttype/
---
## MailMergeSettings.MainDocumentType property

指定邮件合并主文档类型。 默认值为Default.

```csharp
public MailMergeMainDocumentType MainDocumentType { get; set; }
```

## 评论

主文档是包含与合并文档的每个版本相同的信息的文档。

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

* enum [MailMergeMainDocumentType](../../mailmergemaindocumenttype/)
* class [MailMergeSettings](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
