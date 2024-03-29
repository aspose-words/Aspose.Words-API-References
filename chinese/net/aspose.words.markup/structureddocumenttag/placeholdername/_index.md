---
title: StructuredDocumentTag.PlaceholderName
linktitle: PlaceholderName
articleTitle: PlaceholderName
second_title: 用于 .NET 的 Aspose.Words
description: StructuredDocumentTag PlaceholderName 财产. 获取或设置名称BuildingBlock包含占位符文本 在 C#.
type: docs
weight: 240
url: /zh/net/aspose.words.markup/structureddocumenttag/placeholdername/
---
## StructuredDocumentTag.PlaceholderName property

获取或设置名称[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/)包含占位符文本。

[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/)用这个名字[`Name`](../../../aspose.words.buildingblocks/buildingblock/name/)必须存在于[`GlossaryDocument`](../../../aspose.words/document/glossarydocument/) 否则InvalidOperationException会发生。

```csharp
public string PlaceholderName { get; set; }
```

## 例子

演示如何使用构建块的内容作为结构化文档标记的自定义占位符文本。

```csharp
Document doc = new Document();

// 插入“PlainText”类型的纯文本结构化文档标签，该标签将用作文本框。
// 默认显示的内容是“点击此处输入文字”。迅速的。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// 我们可以让标签显示构建块的内容而不是默认文本。
// 首先，将包含内容的构建块添加到术语表文档中。
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// 然后，使用结构化文档标记的“PlaceholderName”属性按名称引用该构建块。
tag.PlaceholderName = "Custom Placeholder";

// 如果“PlaceholderName”引用父文档词汇表文档中的现有块，
// 我们将能够通过“Placeholder”属性验证构建块。
Assert.AreEqual(substituteBlock, tag.Placeholder);

// 将“IsShowingPlaceholderText”属性设置为“true”以处理
// 结构化文档标签的当前内容作为占位符文本。
// 这意味着单击 Microsoft Word 中的文本框将立即突出显示所有标记的内容。
// 将“IsShowingPlaceholderText”属性设置为“false”以获取
// 结构化文档标记，将其内容视为用户已输入的文本。
// 在 Microsoft Word 中单击此文本会将闪烁的光标放置在单击的位置。
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
