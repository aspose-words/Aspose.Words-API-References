---
title: IStructuredDocumentTag.IsShowingPlaceholderText
linktitle: IsShowingPlaceholderText
articleTitle: IsShowingPlaceholderText
second_title: Aspose.Words for .NET
description: 发现 IStructuredDocumentTag IsShowingPlaceholderText 属性，轻松识别 SDT 中的占位符文本，增强内容清晰度和管理性。
type: docs
weight: 50
url: /zh/net/aspose.words.markup/istructureddocumenttag/isshowingplaceholdertext/
---
## IStructuredDocumentTag.IsShowingPlaceholderText property

指定此内容是否**特殊和差别待遇**应解释为包含占位符文本 （与 SDT 中的常规文本内容相反）。

如果设置为 true，则打开此文档时应恢复此状态（显示占位符文本）。

```csharp
public bool IsShowingPlaceholderText { get; set; }
```

## 例子

展示如何使用构建块的内容作为结构化文档标签的自定义占位符文本。

```csharp
Document doc = new Document();

// 插入“PlainText”类型的纯文本结构化文档标签，它将充当文本框的功能。
// 默认显示的内容是“单击此处输入文本。”的提示。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// 我们可以获取标签来显示构建块的内容而不是默认文本。
// 首先，向词汇表文档添加一个包含内容的构建块。
GlossaryDocument glossaryDoc = doc.GlossaryDocument;

BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "Custom Placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.AppendChild(new Body(glossaryDoc));
substituteBlock.FirstSection.Body.AppendParagraph("Custom placeholder text.");

glossaryDoc.AppendChild(substituteBlock);

// 然后，使用结构化文档标签的“PlaceholderName”属性通过名称引用该构建块。
tag.PlaceholderName = "Custom Placeholder";

// 如果“PlaceholderName”指的是父文档的词汇表中的现有块，
// 我们将能够通过“占位符”属性来验证构建块。
Assert.AreEqual(substituteBlock, tag.Placeholder);

// 将“IsShowingPlaceholderText”属性设置为“true”以处理
// 结构化文档标签的当前内容作为占位符文本。
// 这意味着单击 Microsoft Word 中的文本框将立即突出显示标签的所有内容。
// 将“IsShowingPlaceholderText”属性设置为“false”以获取
// 结构化文档标签将其内容视为用户已输入的文本。
// 在 Microsoft Word 中单击此文本将会把闪烁的光标置于单击的位置。
tag.IsShowingPlaceholderText = isShowingPlaceholderText;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlaceholderBuildingBlock.docx");
```

### 也可以看看

* interface [IStructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
