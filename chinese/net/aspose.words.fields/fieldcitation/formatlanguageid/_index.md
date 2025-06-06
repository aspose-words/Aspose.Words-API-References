---
title: FieldCitation.FormatLanguageId
linktitle: FormatLanguageId
articleTitle: FormatLanguageId
second_title: Aspose.Words for .NET
description: 了解 FieldCitation FormatLanguageId 属性如何通过管理书目样式的语言 ID 来增强文档中的引用格式。
type: docs
weight: 30
url: /zh/net/aspose.words.fields/fieldcitation/formatlanguageid/
---
## FieldCitation.FormatLanguageId property

获取或设置与指定的书目样式结合使用的语言 ID，以格式化文档中的引用。

```csharp
public string FormatLanguageId { get; set; }
```

## 例子

展示如何使用 CITATION 和 BIBLIOGRAPHY 字段。

```csharp
// 打开一个包含我们可以在其中找到的书目来源的文档
// Microsoft Word 通过参考 -> 引文和参考书目 -> 管理来源。
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// 仅使用所引用书籍的页码和作者来创建引文。
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// 我们使用标签名称来引用来源。
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// 创建更详细的引用，引用两个来源。
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
fieldBibliography.FormatLanguageId = "5129";
fieldBibliography.FilterLanguageId = "5129";
fieldBibliography.SourceTag = "Book2";

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129 \\f 5129 \\m Book2", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### 也可以看看

* class [FieldCitation](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
