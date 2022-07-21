---
title: MailMergeSettings
second_title: Aspose.Words for .NET API 参考
description: 指定文档的所有邮件合并信息
type: docs
weight: 5550
url: /zh/net/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class

指定文档的所有邮件合并信息。

```csharp
public class MailMergeSettings
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [MailMergeSettings](mailmergesettings)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [ActiveRecord](../../aspose.words.settings/mailmergesettings/activerecord) { get; set; } | 指定应在 Microsoft Word 中显示的数据源记录的从 1 开始的索引。默认值为 1. |
| [AddressFieldName](../../aspose.words.settings/mailmergesettings/addressfieldname) { get; set; } | 指定数据源中包含电子邮件地址的列。默认值为空字符串。 |
| [CheckErrors](../../aspose.words.settings/mailmergesettings/checkerrors) { get; set; } | 指定在执行邮件合并时应由 Microsoft Word 执行的错误报告类型。 默认值为Default. |
| [ConnectString](../../aspose.words.settings/mailmergesettings/connectstring) { get; set; } | 指定用于连接到外部数据源的连接字符串。默认值为空字符串。 |
| [DataSource](../../aspose.words.settings/mailmergesettings/datasource) { get; set; } | 指定邮件合并数据源的路径。默认值为空字符串。 |
| [DataType](../../aspose.words.settings/mailmergesettings/datatype) { get; set; } | 指定邮件合并数据源的类型和数据访问的方法。 默认值为Default. |
| [Destination](../../aspose.words.settings/mailmergesettings/destination) { get; set; } | 指定 Microsoft Word 将如何输出邮件合并的结果。 默认值为Default. |
| [DoNotSupressBlankLines](../../aspose.words.settings/mailmergesettings/donotsupressblanklines) { get; set; } | 指定执行邮件合并的应用程序应如何处理由邮件合并产生的合并文档中的空白行。 默认值为`错误的`. |
| [HeaderSource](../../aspose.words.settings/mailmergesettings/headersource) { get; set; } | 指定邮件合并标头源的路径。 默认值为空字符串。 |
| [LinkToQuery](../../aspose.words.settings/mailmergesettings/linktoquery) { get; set; } | 不确定这个。 Microsoft Word 自动化参考建议这指定每次在 Microsoft Word 中打开文档 时都会执行查询。但是 OOXML 规范建议这指定查询包含一个对包含实际查询的外部查询文件的引用 。 默认值为`错误的`. |
| [MailAsAttachment](../../aspose.words.settings/mailmergesettings/mailasattachment) { get; set; } | 指定在邮件合并操作期间生成的文档应作为附件发送，而不是 ，而不是实际电子邮件的正文。默认值为`错误的`. |
| [MailSubject](../../aspose.words.settings/mailmergesettings/mailsubject) { get; set; } | 指定应出现在邮件合并期间生成的电子邮件或传真的主题行中的文本。 默认值为空字符串。 |
| [MainDocumentType](../../aspose.words.settings/mailmergesettings/maindocumenttype) { get; set; } | 指定邮件合并主文档类型。 默认值为Default. |
| [Odso](../../aspose.words.settings/mailmergesettings/odso) { get; set; } | 获取或设置指定 Office 数据源对象 (ODSO) 设置的对象。 |
| [Query](../../aspose.words.settings/mailmergesettings/query) { get; set; } | 包含应针对指定外部数据源运行的结构化查询语言字符串，以 返回执行邮件合并操作时应导入文档的记录集。 默认值为空字符串。 |
| [ViewMergedData](../../aspose.words.settings/mailmergesettings/viewmergeddata) { get; set; } | 指定 Microsoft Word 应显示来自已插入合并字段 的指定外部数据源的数据（例如预览合并数据）。默认值为`错误的`. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Clear](../../aspose.words.settings/mailmergesettings/clear)() | 清除邮件合并设置，这样当保存文档时 不会保存邮件合并设置，它会变成一个普通的文档。 |
| [Clone](../../aspose.words.settings/mailmergesettings/clone)() | 返回此对象的深层克隆。 |

### 评论

您可以使用此对象为文档指定邮件合并数据源，当用户打开此文档时，此信息 （以及可用的数据字段）将出现在 Microsoft Word 中。 或者您可以使用此对象查询邮件合并设置用户已在 Microsoft Word 中为此文档指定。

您通常不需要直接创建此类的对象，因为文档的邮件合并设置 始终可以通过[`MailMergeSettings`](../../aspose.words/document/mailmergesettings)财产。

要检测此文档是否为邮件合并主文档，请检查 的值[`MainDocumentType`](./maindocumenttype)财产。

要从文档中删除邮件合并设置和数据源信息，您可以使用 [`Clear`](./clear)方法。 Aspose.Words 不会将邮件合并设置写入文档，如果 [`MainDocumentType`](./maindocumenttype)属性设置为NotAMergeDocument 或[`DataType`](./datatype)属性设置为None.

学习如何使用该对象的属性的最佳方法是在 Microsoft Word 中手动创建一个包含所需 数据源的文档，然后使用 Aspose.Words 打开该文档并检查属性 [`MailMergeSettings`](../../aspose.words/document/mailmergesettings)和[`Odso`](./odso)对象。例如，如果您想学习如何以编程方式配置数据源，这是 的好方法。

Aspose.Words 在不同格式之间加载、保存和转换documents 时会保留邮件合并信息，但在使用[`MailMerge`](../../aspose.words.mailmerging/mailmerge)目的。

### 例子

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

// 创建一个ASCII文件形式的数据源，用“|”特点
// 充当分隔列的分隔符。第一行包含三列的名称，
// 之后的每一行都是具有各自值的行。
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

* 命名空间 [Aspose.Words.Settings](../../aspose.words.settings)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
