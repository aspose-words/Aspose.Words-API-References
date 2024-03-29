---
title: FieldCitation.VolumeNumber
linktitle: VolumeNumber
articleTitle: VolumeNumber
second_title: 用于 .NET 的 Aspose.Words
description: FieldCitation VolumeNumber 财产. 获取或设置与引文关联的卷号 在 C#.
type: docs
weight: 110
url: /zh/net/aspose.words.fields/fieldcitation/volumenumber/
---
## FieldCitation.VolumeNumber property

获取或设置与引文关联的卷号。

```csharp
public string VolumeNumber { get; set; }
```

## 例子

展示如何使用 CITATION 和 BIBLIOGRAPHY 字段。

```csharp
// 打开一个包含我们可以找到的书目来源的文档
// Microsoft Word 通过参考文献 ->引文与参考书目->管理来源。
Document doc = new Document(MyDir + "Bibliography.docx");
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Text to be cited with one source.");

// 创建仅包含参考书籍的页码和作者的引文。
FieldCitation fieldCitation = (FieldCitation)builder.InsertField(FieldType.FieldCitation, true);

// 我们使用标签名称来引用源。
fieldCitation.SourceTag = "Book1";
fieldCitation.PageNumber = "85";
fieldCitation.SuppressAuthor = false;
fieldCitation.SuppressTitle = true;
fieldCitation.SuppressYear = true;

Assert.AreEqual(" CITATION  Book1 \\p 85 \\t \\y", fieldCitation.GetFieldCode());

// 创建引用两个来源的更详细的引文。
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

Assert.AreEqual(" BIBLIOGRAPHY  \\l 5129", fieldBibliography.GetFieldCode());

doc.UpdateFields();
doc.Save(ArtifactsDir + "Field.CITATION.docx");
```

### 也可以看看

* class [FieldCitation](../)
* 命名空间 [Aspose.Words.Fields](../../../aspose.words.fields/)
* 部件 [Aspose.Words](../../../)
