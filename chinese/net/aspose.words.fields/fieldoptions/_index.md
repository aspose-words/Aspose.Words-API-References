---
title: FieldOptions Class
linktitle: FieldOptions
articleTitle: FieldOptions
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Fields.FieldOptions 班级. 表示控制文档中的字段处理的选项 在 C#.
type: docs
weight: 2250
url: /zh/net/aspose.words.fields/fieldoptions/
---
## FieldOptions class

表示控制文档中的字段处理的选项。

```csharp
public sealed class FieldOptions
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BarcodeGenerator](../../aspose.words.fields/fieldoptions/barcodegenerator/) { get; set; } | 获取或设置自定义条码生成器。 |
| [BibliographyStylesProvider](../../aspose.words.fields/fieldoptions/bibliographystylesprovider/) { get; set; } |  |
| [BuiltInTemplatesPaths](../../aspose.words.fields/fieldoptions/builtintemplatespaths/) { get; set; } | 获取或设置 MS Word 内置模板的路径。 |
| [ComparisonExpressionEvaluator](../../aspose.words.fields/fieldoptions/comparisonexpressionevaluator/) { get; set; } | 获取或设置字段比较表达式求值器。 |
| [CurrentUser](../../aspose.words.fields/fieldoptions/currentuser/) { get; set; } | 获取或设置当前用户信息 |
| [CustomTocStyleSeparator](../../aspose.words.fields/fieldoptions/customtocstyleseparator/) { get; set; } | 获取或设置 \t 开关的自定义样式分隔符[`FieldToc`](../fieldtoc/)字段. |
| [DefaultDocumentAuthor](../../aspose.words.fields/fieldoptions/defaultdocumentauthor/) { get; set; } | 获取或设置默认文档作者的姓名。如果已在内置文档属性中指定作者姓名， 不考虑此选项。 |
| [FieldDatabaseProvider](../../aspose.words.fields/fieldoptions/fielddatabaseprovider/) { get; set; } | 获取或设置返回查询结果的提供程序[`FieldDatabase`](../fielddatabase/)字段. |
| [FieldIndexFormat](../../aspose.words.fields/fieldoptions/fieldindexformat/) { get; set; } | 获取或设置一个[`FieldIndexFormat`](./fieldindexformat/)代表 的格式[`FieldIndex`](../fieldindex/)文档中的字段. |
| [FieldUpdateCultureProvider](../../aspose.words.fields/fieldoptions/fieldupdatecultureprovider/) { get; set; } | 获取或设置一个提供程序，该提供程序返回特定于每个特定字段的区域性对象。 |
| [FieldUpdateCultureSource](../../aspose.words.fields/fieldoptions/fieldupdateculturesource/) { get; set; } | 指定用于格式化字段结果的区域性。 |
| [FieldUpdatingCallback](../../aspose.words.fields/fieldoptions/fieldupdatingcallback/) { get; set; } | 获取或设置[`IFieldUpdatingCallback`](../ifieldupdatingcallback/)实施 |
| [FieldUpdatingProgressCallback](../../aspose.words.fields/fieldoptions/fieldupdatingprogresscallback/) { get; set; } |  |
| [FileName](../../aspose.words.fields/fieldoptions/filename/) { get; set; } | 获取或设置文档的文件名。 |
| [IsBidiTextSupportedOnUpdate](../../aspose.words.fields/fieldoptions/isbiditextsupportedonupdate/) { get; set; } | 获取或设置字段更新时是否完全支持双向文本的值。 |
| [LegacyNumberFormat](../../aspose.words.fields/fieldoptions/legacynumberformat/) { get; set; } | 获取或设置指示是否启用字段的旧版（早于 AW 13.10）数字格式的值。 |
| [PreProcessCulture](../../aspose.words.fields/fieldoptions/preprocessculture/) { get; set; } | 获取或设置区域性以预处理字段值。 |
| [ResultFormatter](../../aspose.words.fields/fieldoptions/resultformatter/) { get; set; } | 允许控制字段结果的格式。 |
| [TemplateName](../../aspose.words.fields/fieldoptions/templatename/) { get; set; } | 获取或设置文档使用的模板的文件名。 |
| [ToaCategories](../../aspose.words.fields/fieldoptions/toacategories/) { get; set; } | 获取或设置权限类别表。 |
| [UseInvariantCultureNumberFormat](../../aspose.words.fields/fieldoptions/useinvariantculturenumberformat/) { get; set; } | 获取或设置数值格式是否使用不变区域性解析 |
| [UserPromptRespondent](../../aspose.words.fields/fieldoptions/userpromptrespondent/) { get; set; } | 获取或设置字段更新期间对用户提示的响应者。 |

## 例子

显示如何在字段更新或邮件合并期间指定用于日期格式的文化来源。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入两个使用德语区域设置的合并字段。
builder.Font.LocaleId = new CultureInfo("de-DE").LCID;
builder.InsertField("MERGEFIELD Date1 \\@ \"dddd, d MMMM yyyy\"");
builder.Write(" - ");
builder.InsertField("MERGEFIELD Date2 \\@ \"dddd, d MMMM yyyy\"");

// 在变量中保留其原始值后，将当前文化设置为美国英语。
CultureInfo currentCulture = Thread.CurrentThread.CurrentCulture;
Thread.CurrentThread.CurrentCulture = new CultureInfo("en-US");

// 此合并将使用当前线程的文化来格式化日期，美国英语。
doc.MailMerge.Execute(new[] { "Date1" }, new object[] { new DateTime(2020, 1, 01) });

// 配置下一个合并以从字段代码中获取其文化值。这种文化的价值将是德国的。
doc.FieldOptions.FieldUpdateCultureSource = FieldUpdateCultureSource.FieldCode;
doc.MailMerge.Execute(new[] { "Date2" }, new object[] { new DateTime(2020, 1, 01) });

// 第一个合并结果包含一个英文格式的日期，而第二个是德文的。
Assert.AreEqual("Wednesday, 1 January 2020 - Mittwoch, 1 Januar 2020", doc.Range.Text.Trim());

// 恢复线程的原始文化。
Thread.CurrentThread.CurrentCulture = currentCulture;
```

### 也可以看看

* 命名空间 [Aspose.Words.Fields](../../aspose.words.fields/)
* 部件 [Aspose.Words](../../)
