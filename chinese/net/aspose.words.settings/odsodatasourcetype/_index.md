---
title: OdsoDataSourceType Enum
linktitle: OdsoDataSourceType
articleTitle: OdsoDataSourceType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words OdsoDataSourceType 枚举，轻松连接到外部数据源，增强您的文档处理能力。
type: docs
weight: 6720
url: /zh/net/aspose.words.settings/odsodatasourcetype/
---
## OdsoDataSourceType enumeration

指定作为 ODSO 连接信息的一部分要连接的外部数据源的类型。

```csharp
public enum OdsoDataSourceType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Text | `0` | 指定给定文档已连接到文本文件。 可能为 wdMergeSubTypeOther。 |
| Database | `1` | 指定给定文档已连接到数据库。 可能为 wdMergeSubTypeAccess。 |
| AddressBook | `2` | 指定给定文档已连接到联系人地址簿。 可能为 wdMergeSubTypeOAL。 |
| Document1 | `3` | 指定给定文档已连接到生成应用程序支持的另一种文档格式。 可能是 wdMergeSubTypeOLEDBWord。 |
| Document2 | `4` | 指定给定文档已连接到生成应用程序支持的另一种文档格式。 可能是 wdMergeSubTypeWorks。 |
| Native | `5` | 指定给定文档已连接到生成应用程序的另一种文档格式。 可能是 wdMergeSubTypeOLEDBText |
| Email | `6` | 指定给定文档已连接到电子邮件应用程序。 可能为 wdMergeSubTypeOutlook。 |
| None | `7` | 未指定外部数据源的类型。 可能是 wdMergeSubTypeWord。 |
| Legacy | `8` | 指定给定文档已连接到生成应用程序支持的旧文档格式 可能是 wdMergeSubTypeWord2000. |
| Master | `9` | 指定给定文档已连接到聚合其他数据源的数据源。 |
| Default | `7` | 等于None. |

## 评论

OOXML 规范对这个枚举的定义非常模糊。我猜它可能对应 WdMergeSubType 枚举 http://msdn.microsoft.com/en-us/library/bb237801.aspx。

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

* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
