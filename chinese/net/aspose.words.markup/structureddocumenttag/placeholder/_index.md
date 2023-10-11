---
title: StructuredDocumentTag.Placeholder
second_title: Aspose.Words for .NET API 参考
description: StructuredDocumentTag 财产. 获取BuildingBlock包含当此 SDT 运行内容为空时应显示的占位符文本 关联的映射 XML 元素为空如通过XmlMappingelement 或IsShowingPlaceholderText元素是真的.
type: docs
weight: 230
url: /zh/net/aspose.words.markup/structureddocumenttag/placeholder/
---
## StructuredDocumentTag.Placeholder property

获取[`BuildingBlock`](../../../aspose.words.buildingblocks/buildingblock/)包含当此 SDT 运行内容为空时应显示的占位符文本， 关联的映射 XML 元素为空，如通过[`XmlMapping`](../xmlmapping/)element 或[`IsShowingPlaceholderText`](../isshowingplaceholdertext/)元素是`真的`.

```csharp
public BuildingBlock Placeholder { get; }
```

### 评论

可`无效的`，表示占位符不适用于此 Sdt。

### 例子

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

* class [BuildingBlock](../../../aspose.words.buildingblocks/buildingblock/)
* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../structureddocumenttag/)
* 部件 [Aspose.Words](../../../)


