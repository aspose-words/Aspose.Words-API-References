---
title: MailMergeMainDocumentType Enum
linktitle: MailMergeMainDocumentType
articleTitle: MailMergeMainDocumentType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.MailMergeMainDocumentType 枚举，定义各种邮件合并源文档类型，实现无缝文档自动化。
type: docs
weight: 6670
url: /zh/net/aspose.words.settings/mailmergemaindocumenttype/
---
## MailMergeMainDocumentType enumeration

指定邮件合并源文档的可能类型。

```csharp
public enum MailMergeMainDocumentType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| NotAMergeDocument | `0` | 此文档不是邮件合并文档。 |
| FormLetters | `1` | 指定邮件合并源文档为格式信函类型。 |
| MailingLabels | `2` | 指定邮件合并源文档属于邮件标签类型。 |
| Envelopes | `4` | 指定邮件合并源文档为信封类型。 |
| Catalog | `8` | 指定邮件合并源文档属于目录类型。 |
| Email | `16` | 指定邮件合并源文档属于电子邮件类型。 |
| Fax | `32` | 指定邮件合并源文档为传真类型。 |
| Default | `0` | 等于NotAMergeDocument |

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

* property [MainDocumentType](../mailmergesettings/maindocumenttype/)
* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
