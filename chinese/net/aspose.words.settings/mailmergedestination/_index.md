---
title: MailMergeDestination Enum
linktitle: MailMergeDestination
articleTitle: MailMergeDestination
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.MailMergeDestination 枚举，定义无缝文档邮件合并的结果。立即优化您的文档处理！
type: docs
weight: 6660
url: /zh/net/aspose.words.settings/mailmergedestination/
---
## MailMergeDestination enumeration

指定在文档上执行邮件合并时可能生成的结果。

```csharp
public enum MailMergeDestination
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| NewDocument | `0` | 指定符合要求的托管应用程序应通过使用来自指定外部数据源的数据填充给定文档中的字段来生成新文档。 |
| Printer | `1` | 指定符合要求的托管应用程序应打印使用来自指定外部数据源的外部数据填充给定文档中的 字段所产生的文档。 |
| Email | `2` | 指定符合要求的托管应用程序应使用由来自指定外部数据源的数据填充给定文档中的字段而生成的文档来生成电子邮件。 |
| Fax | `4` | 指定符合要求的托管应用程序应使用由来自指定外部数据源的数据填充给定文档中的字段而生成的文档来生成传真。 |
| Default | `0` | 等于NewDocument值. |

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

* property [Destination](../mailmergesettings/destination/)
* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
