---
title: Odso Class
linktitle: Odso
articleTitle: Odso
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Settings.Odso 班级. 指定邮件合并数据源的 Office 数据源对象 ODSO 设置 在 C#.
type: docs
weight: 5880
url: /zh/net/aspose.words.settings/odso/
---
## Odso class

指定邮件合并数据源的 Office 数据源对象 (ODSO) 设置。

要了解更多信息，请访问[邮件合并和报告](https://docs.aspose.com/words/net/mail-merge-and-reporting/)文档文章。

```csharp
public class Odso
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Odso](odso/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ColumnDelimiter](../../aspose.words.settings/odso/columndelimiter/) { get; set; } | 指定应解释为用于分隔外部数据源中的列的列分隔符的字符。 默认值为 0，这意味着没有定义列分隔符。 |
| [DataSource](../../aspose.words.settings/odso/datasource/) { get; set; } | 指定要连接到文档以执行邮件合并的外部数据源的位置。 默认值为空字符串。 |
| [DataSourceType](../../aspose.words.settings/odso/datasourcetype/) { get; set; } | 指定要连接到的外部数据源的类型，作为此邮件合并的 ODSO 连接信息的一部分。 默认值为Default. |
| [FieldMapDatas](../../aspose.words.settings/odso/fieldmapdatas/) { get; set; } | 获取或设置对象集合，这些对象指定如何将外部数据源 中的列映射到文档中的预定义合并字段名称。 该对象从不`无效的`. |
| [FirstRowContainsColumnNames](../../aspose.words.settings/odso/firstrowcontainscolumnnames/) { get; set; } | 指定托管应用程序应将指定外部数据 源中的第一行数据视为包含数据源中每列名称的标题行。 默认值为`错误的`. |
| [RecipientDatas](../../aspose.words.settings/odso/recipientdatas/) { get; set; } | 获取或设置指定在邮件合并中包含/排除单个记录的对象集合。 该对象从不`无效的`. |
| [TableName](../../aspose.words.settings/odso/tablename/) { get; set; } | 指定源应在外部数据源内连接到的特定数据集。 默认值为空字符串。 |
| [UdlConnectString](../../aspose.words.settings/odso/udlconnectstring/) { get; set; } | 指定用于连接到外部数据源的通用数据链接 (UDL) 连接字符串。 默认值为空字符串。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clone](../../aspose.words.settings/odso/clone/)() | 返回此对象的深度克隆。 |

## 评论

ODSO 似乎是较新的 Microsoft Word 版本在为邮件合并文档指定某些 类型的数据源时更喜欢使用的“新”方式。 ODSO 可能首先出现在 Microsoft Word 2000 中。

ODSO 的使用记录很少，了解如何使用此对象 的属性的最佳方法是在 Microsoft Word 中手动创建具有所需数据源的文档，然后使用 Aspose.Words 打开该文档并检查属性的[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/)和 [`Odso`](../mailmergesettings/odso/)对象。例如，如果您想了解如何 以编程方式配置数据源，那么这是一个很好的方法。

您通常不需要直接创建此类的对象，因为 ODSO settings 始终可通过[`Odso`](../mailmergesettings/odso/)财产。

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

* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings/)
* 部件 [Aspose.Words](../../)
