---
title: ParagraphFormat.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat Bidi 财产. 获取或设置这是否是从右到左的段落 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words/paragraphformat/bidi/
---
## ParagraphFormat.Bidi property

获取或设置这是否是从右到左的段落。

```csharp
public bool Bidi { get; set; }
```

## 评论

如果为 true，则此段落 中的运行和其他内联对象从右到左排列。

## 例子

显示如何检测纯文本文档的文本方向。

```csharp
// 创建一个“TxtLoadOptions”对象，我们可以将它传递给文档的构造函数
// 修改我们加载纯文本文档的方式。
TxtLoadOptions loadOptions = new TxtLoadOptions();

// 将“DocumentDirection”属性设置为“DocumentDirection.Auto”自动检测
// Aspose.Words 从纯文本加载的每一段文本的方向。
// 每个段落的“Bidi”属性都会存储它的方向。
loadOptions.DocumentDirection = DocumentDirection.Auto;

// 检测从右到左的希伯来语文本。
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// 将英文文本检测为从右到左。
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

展示如何使用 BIDIOUTLINE 字段创建从右到左的语言兼容列表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// BIDIOUTLINE 字段编号段落，如 AUTONUM/LISTNUM 字段，
// 但仅在启用从右到左的编辑语言时可见，例如希伯来语或阿拉伯语。
// 以下字段将显示“.1”，即列表编号“1.”的 RTL 等效项。
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// 添加另外两个 BIDIOUTLINE 字段，将显示“.2”和“.3”。
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");
builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

// 将文档中每个段落的水平文本对齐方式设置为 RTL。
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
{
    para.ParagraphFormat.Bidi = true;
}

// 如果我们在 Microsoft Word 中启用从右到左的编辑语言，我们的字段将显示数字。
// 否则，它们将显示“###”。
doc.Save(ArtifactsDir + "Field.BIDIOUTLINE.docx");
```

### 也可以看看

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
