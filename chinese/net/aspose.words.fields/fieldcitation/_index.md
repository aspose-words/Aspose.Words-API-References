---
title: FieldCitation
second_title: Aspose.Words for .NET API 参考
description: 实现 CITATION 字段
type: docs
weight: 1510
url: /zh/net/aspose.words.fields/fieldcitation/
---
## FieldCitation class

实现 CITATION 字段。

```csharp
public class FieldCitation : Field
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [FieldCitation](fieldcitation)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AnotherSourceTag](../../aspose.words.fields/fieldcitation/anothersourcetag) { get; set; } | 获取或设置一个值，该值计算 **标签** 元素的值引用。 |
| [DisplayResult](../../aspose.words.fields/field/displayresult) { get; } | 获取表示显示字段结果的文本。 |
| [End](../../aspose.words.fields/field/end) { get; } | 获取表示字段结束的节点。 |
| [Format](../../aspose.words.fields/field/format) { get; } | 获取[`FieldFormat`](../fieldformat)对象，该对象提供对字段格式的类型化访问。 |
| [FormatLanguageId](../../aspose.words.fields/fieldcitation/formatlanguageid) { get; set; } | 获取或设置与指定书目样式结合使用的语言 ID，以格式化文档中的引用 。 |
| [IsDirty](../../aspose.words.fields/field/isdirty) { get; set; } | 获取或设置字段的当前结果是否由于对文档的其他修改而不再正确（陈旧）。 |
| [IsLocked](../../aspose.words.fields/field/islocked) { get; set; } | 获取或设置字段是否被锁定（不应重新计算其结果）。 |
| [LocaleId](../../aspose.words.fields/field/localeid) { get; set; } | 获取或设置字段的 LCID。 |
| [PageNumber](../../aspose.words.fields/fieldcitation/pagenumber) { get; set; } | 获取或设置与引文相关的页码。 |
| [Prefix](../../aspose.words.fields/fieldcitation/prefix) { get; set; } | 获取或设置在引文前面的前缀。 |
| [Result](../../aspose.words.fields/field/result) { get; set; } | 获取或设置字段分隔符和字段结尾之间的文本。 |
| [Separator](../../aspose.words.fields/field/separator) { get; } | 获取表示字段分隔符的节点。可以为空。 |
| [SourceTag](../../aspose.words.fields/fieldcitation/sourcetag) { get; set; } | 获取或设置一个值，该值计算 **标签** 要插入的源元素的值。 |
| [Start](../../aspose.words.fields/field/start) { get; } | 获取表示字段开始的节点。 |
| [Suffix](../../aspose.words.fields/fieldcitation/suffix) { get; set; } | 获取或设置附加到引文的后缀。 |
| [SuppressAuthor](../../aspose.words.fields/fieldcitation/suppressauthor) { get; set; } | 获取或设置作者信息是否从引文中隐藏。 |
| [SuppressTitle](../../aspose.words.fields/fieldcitation/suppresstitle) { get; set; } | 获取或设置是否从引文中抑制标题信息。 |
| [SuppressYear](../../aspose.words.fields/fieldcitation/suppressyear) { get; set; } | 获取或设置是否从引文中抑制年份信息。 |
| virtual [Type](../../aspose.words.fields/field/type) { get; } | 获取 Microsoft Word 字段类型。 |
| [VolumeNumber](../../aspose.words.fields/fieldcitation/volumenumber) { get; set; } | 获取或设置与引文相关的卷号。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)() | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 包含子字段的字段代码和字段结果。 |
| [GetFieldCode](../../aspose.words.fields/field/getfieldcode)(bool) | 返回字段开始和字段分隔符之间的文本（如果没有分隔符，则返回字段结束）。 |
| [Remove](../../aspose.words.fields/field/remove)() | 从文档中删除字段。在字段之后返回一个节点。如果字段的结尾是其父节点的最后一个子 ，则返回其父段落。如果该字段已被删除，则返回 **null** 。 |
| [Unlink](../../aspose.words.fields/field/unlink)() | 执行字段取消链接。 |
| [Update](../../aspose.words.fields/field/update)() | 执行字段更新。如果该字段已被更新，则抛出。 |
| [Update](../../aspose.words.fields/field/update)(bool) | 执行字段更新。如果该字段已被更新，则抛出。 |

### 评论

插入 **Source**的内容 元素，具有指定的 **标签** 使用书目样式的元素。

### 例子

显示如何使用 CITATION 和 BIBLIOGRAPHY 字段。

```csharp
// 打开一个包含我们可以在其中找到的书目来源的文档
// Microsoft Word via References ->引文与参考书目 ->管理来源。
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// 创建仅包含页码和参考书作者的引文。
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// 我们使用它们的标签名称来引用源。
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// 创建一个引用两个来源的更详细的引文。
builder.InsertParagraph();
builder.Write("Text to be cited with two sources.");
fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);
fieldCitation.SourceTag = "Book1";
fieldCitation.AnotherSourceTag = "Book2";
fieldCitation.FormatLanguageId = "en-US";
fieldCitation.PageNumber = "19";
fieldCitation.Prefix = "Prefix ";
fieldCitation.Suffix = " Suffix";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = false;
fieldCitation.SuppressYear = false;
fieldCitation.VolumeNumber = "VII";

Assert.AreEqual(" CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f \"Prefix \" \\s \" Suffix\" \\v VII", fieldCitation.GetFieldCode());

// 我们可以使用 BIBLIOGRAPHY 字段来显示文档中的所有来源。
builder.InsertBreak(BreakType.PageBreak);
FieldBibliography fieldBibliography = (FieldBibliography)builder.InsertField(FieldType.FieldBibliography, true);
fieldBibliography.FormatLanguageId = "1124";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 1124", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### 也可以看看

* class [Field](../field)
* namespace [Aspose.Words.Fields](../../aspose.words.fields)
* assembly [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
