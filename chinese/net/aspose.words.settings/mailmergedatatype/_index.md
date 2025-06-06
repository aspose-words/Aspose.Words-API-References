---
title: MailMergeDataType Enum
linktitle: MailMergeDataType
articleTitle: MailMergeDataType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.MailMergeDataType 枚举，以便在文档自动化项目中无缝集成外部数据源。
type: docs
weight: 6650
url: /zh/net/aspose.words.settings/mailmergedatatype/
---
## MailMergeDataType enumeration

指定外部邮件合并数据源的类型。

```csharp
public enum MailMergeDataType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `-1` | 未指定邮件合并数据源。 |
| TextFile | `0` | 指定给定文档已通过动态数据交换 (DDE) 系统连接到文本文件。 |
| Database | `1` | 指定给定文档已通过动态数据交换 (DDE) 系统连接到 Access 数据库。 |
| Spreadsheet | `2` | 指定给定文档已通过动态数据交换 (DDE) 系统连接到 Excel 电子表格。 |
| Query | `3` | 指定给定文档已使用外部查询工具连接到外部数据源。 |
| Odbc | `4` | 指定给定文档已通过开放数据库连接接口连接到外部数据源。 |
| Native | `5` | 指定给定文档已通过 Office 数据源对象 (ODSO) 接口连接到外部数据源。 |
| Default | `-1` | 等于None. |

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

* property [DataType](../mailmergesettings/datatype/)
* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
