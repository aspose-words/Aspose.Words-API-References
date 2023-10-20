---
title: StructuredDocumentTag.IsShowingPlaceholderText
linktitle: IsShowingPlaceholderText
articleTitle: IsShowingPlaceholderText
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTag IsShowingPlaceholderText 财产. 指定此内容是否SDT应被解释为包含占位符 text 与 SDT 中的常规文本内容相反 在 C#.
type: docs
weight: 150
url: /zh/net/aspose.words.markup/structureddocumenttag/isshowingplaceholdertext/
---
## StructuredDocumentTag.IsShowingPlaceholderText property

指定此内容是否**SDT**应被解释为包含占位符 text （与 SDT 中的常规文本内容相反）。

如果设置为 true，则在打开此文档时应恢复此状态（显示占位符文本）。

```csharp
public bool IsShowingPlaceholderText { get; set; }
```

## 例子

展示如何将构建基块的内容用作结构化文档标签的自定义占位符文本。

```csharp
Document doc = new Document();

// 插入“PlainText”类型的纯文本结构化文档标签，该标签将用作文本框。
// 默认显示的内容是“点击这里输入文字”。迅速的。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// 我们可以让标签显示构建块的内容而不是默认文本。
// 首先，在词汇表文档中添加一个包含内容的构建块。
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// 然后，使用结构化文档标签的“PlaceholderName”属性按名称引用该构建块。
tag.PlaceholderName = "Custom Placeholder";

// 如果“PlaceholderName”引用父文档的词汇表文档中的现有块，
// 我们将能够通过“Placeholder”属性验证构建块。
Assert.AreEqual(substituteBlock, tag.Placeholder);

// 将“IsShowingPlaceholderText”属性设置为“true”以处理
// 结构化文档标签的当前内容作为占位符文本。
// 这意味着单击 Microsoft Word 中的文本框将立即突出显示所有标记的内容。
// 将“IsShowingPlaceholderText”属性设置为“false”以获取
// 结构化文档标签，将其内容视为用户已经输入的文本。
// 在 Microsoft Word 中单击此文本会将闪烁的光标置于单击的位置。
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
