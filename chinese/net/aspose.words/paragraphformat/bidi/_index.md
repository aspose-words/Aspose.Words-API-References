---
title: ParagraphFormat.Bidi
linktitle: Bidi
articleTitle: Bidi
second_title: Aspose.Words for .NET
description: 发现 ParagraphFormat Bidi 属性可以轻松控制从右到左的文本格式，从而增强可读性并改善文档布局。
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

什么时候`真的`，此段落 中的运行和其他内联对象从右到左布局。

## 例子

展示如何检测纯文本文档的文本方向。

```csharp
// 创建一个“TxtLoadOptions”对象，我们可以将其传递给文档的构造函数
// 修改我们加载纯文本文档的方式。
TxtLoadOptions loadOptions = new TxtLoadOptions();

// 将“DocumentDirection”属性设置为“DocumentDirection.Auto”自动检测
// Aspose.Words 从纯文本加载的每个文本段落的方向。
// 每个段落的“Bidi”属性将存储其方向。
loadOptions.DocumentDirection = DocumentDirection.Auto;

// 将希伯来语文本检测为从右到左。
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// 检测英文文本是否从右到左。
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

展示如何使用 BIDIOUTLINE 字段创建从右到左的语言兼容列表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// BIDIOUTLINE 字段像 AUTONUM/LISTNUM 字段一样对段落进行编号，
// 但仅在启用从右到左的编辑语言（例如希伯来语或阿拉伯语）时才可见。
// 以下字段将显示“.1”，即列表编号“1.”的 RTL 等效项。
FieldBidiOutline field = (FieldBidiOutline)builder.InsertField(FieldType.FieldBidiOutline, true);
builder.Writeln("שלום");

Assert.AreEqual(" BIDIOUTLINE ", field.GetFieldCode());

// 再添加两个 BIDIOUTLINE 字段，分别显示“.2”和“.3”。
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
