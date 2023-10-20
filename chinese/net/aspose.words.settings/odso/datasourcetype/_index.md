---
title: Odso.DataSourceType
linktitle: DataSourceType
articleTitle: DataSourceType
second_title: 用于 .NET 的 Aspose.Words
description: Odso DataSourceType 财产. 指定要连接到的外部数据源的类型作为此邮件合并的 ODSO 连接信息的一部分 默认值为Default 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.settings/odso/datasourcetype/
---
## Odso.DataSourceType property

指定要连接到的外部数据源的类型，作为此邮件合并的 ODSO 连接信息的一部分。 默认值为Default.

```csharp
public OdsoDataSourceType DataSourceType { get; set; }
```

## 评论

此设置纯粹是用于此邮件合并的数据源类型的建议。

## 例子

演示如何使用 Office 数据源对象中的数据执行邮件合并。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Dear ");
builder.InsertField("MERGEFIELD FirstName", "<FirstName>");
builder.Write(" ");
builder.InsertField("MERGEFIELD LastName", "<LastName>");
builder.Writeln(": ");
builder.InsertField("MERGEFIELD Message", "<Message>");

// 创建一个ASCII文件形式的数据源，带有“|”特点
// 充当分隔列的分隔符。第一行包含三列的名称，
// 随后的每一行都是具有各自值的行。
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

* enum [OdsoDataSourceType](../../odsodatasourcetype/)
* class [Odso](../)
* 命名空间 [Aspose.Words.Settings](../../../aspose.words.settings/)
* 部件 [Aspose.Words](../../../)
