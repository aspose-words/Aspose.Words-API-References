---
title: MailMergeSettings Class
linktitle: MailMergeSettings
articleTitle: MailMergeSettings
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.MailMergeSettings 类，通过强大的邮件合并功能简化文档自动化，从而提高效率。
type: docs
weight: 6680
url: /zh/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

指定文档的所有邮件合并信息。

要了解更多信息，请访问[邮件合并和报告](https://docs.aspose.com/words/net/mail-merge-and-reporting/)文档文章。

```csharp
public class MailMergeSettings
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [MailMergeSettings](mailmergesettings/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord/) { get; set; } | 指定数据源中记录的从一开始的索引，该索引应显示在 Microsoft Word 中。默认值为 1。 |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname/) { get; set; } | 指定数据源中包含电子邮件地址的列。默认值为空字符串。 |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors/) { get; set; } | 指定 Microsoft Word 在执行邮件合并时应进行的错误报告类型。 默认值为Default. |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring/) { get; set; } | 指定用于连接外部数据源的连接字符串。默认值为空字符串。 |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource/) { get; set; } | 指定邮件合并数据源的路径。默认值为空字符串。 |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype/) { get; set; } | 指定邮件合并数据源的类型和数据访问方法。 默认值为Default. |
| [Destination](../../aspose.words.settings/mailmergesettings/destination/) { get; set; } | 指定 Microsoft Word 如何输出邮件合并的结果。 默认值为Default. |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines/) { get; set; } | 指定执行邮件合并的应用程序应如何处理邮件合并产生的合并文档中的空白行。 默认值为`错误的`. |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource/) { get; set; } | 指定邮件合并标头源的路径。 默认值为空字符串。 |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery/) { get; set; } | 对此不太确定。 Microsoft Word 自动化参考建议，这指定每次在 Microsoft Word 中打开文档 时都会执行查询。但 OOXML 规范建议，这指定查询包含对包含实际查询的外部查询文件的引用 。 默认值为`错误的`. |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment/) { get; set; } | 指定邮件合并操作期间生成的文档应作为附件发送，而不是作为实际电子邮件的正文发送。默认值为`错误的`. |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject/) { get; set; } | 指定邮件合并期间生成的电子邮件或传真主题行中显示的文本。 默认值为空字符串。 |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype/) { get; set; } | 指定邮件合并主文档类型。 默认值为Default. |
| [Odso](../../aspose.words.settings/mailmergesettings/odso/) { get; set; } | 获取或设置指定 Office 数据源对象 (ODSO) 设置的对象。 |
| [Query](../../aspose.words.settings/mailmergesettings/query/) { get; set; } | 包含结构化查询语言字符串，该字符串应针对指定的外部数据源运行，以 返回执行邮件合并操作时应导入文档的记录集。 默认值为空字符串。 |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata/) { get; set; } | 指定 Microsoft Word 应显示来自指定外部数据源的数据，其中已插入合并字段 （例如，预览合并数据）。默认值为`错误的`. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear/)() | 清除邮件合并设置，以便在保存文档时， 不会保存任何邮件合并设置，并且它将成为普通文档。 |
| [Clone](../../aspose.words.settings/mailmergesettings/clone/)() | 返回此对象的深度克隆。 |

## 评论

您可以使用此对象为文档指定邮件合并数据源，并且当用户打开此文档时，此信息 （连同可用的数据字段）将显示在 Microsoft Word 中。 或者您可以使用此对象查询用户在 Microsoft Word 中为此文档指定的邮件合并设置。

通常不需要直接创建此类的对象，因为文档的邮件合并设置 始终可以通过[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/)财产。

要检测此文档是否为邮件合并主文档，请检查 的值[`MainDocumentType`](./maindocumenttype/)财产。

要从文档中删除邮件合并设置和数据源信息，您可以使用 [`Clear`](./clear/)方法。如果 出现错误，Aspose.Words 将不会将邮件合并设置写入文档[`MainDocumentType`](./maindocumenttype/)属性设置为NotAMergeDocument 或[`DataType`](./datatype/)属性设置为None。

学习如何使用此对象的属性的最佳方法是在 Microsoft Word 中手动创建具有所需 数据源的文档，然后使用 Aspose.Words 打开该文档并检查[`MailMergeSettings`](../../aspose.words/document/mailmergesettings/)和[`Odso`](./odso/)对象。例如，如果您想学习如何以编程方式配置数据源，这是一种不错的方法。

Aspose.Words 在加载、保存和转换不同格式的文档时保留邮件合并信息 ，但在使用执行自己的邮件合并 时不使用此信息[`MailMerge`](../../aspose.words.mailmerging/mailmerge/)目的。

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
