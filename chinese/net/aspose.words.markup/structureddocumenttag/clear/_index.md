---
title: StructuredDocumentTag.Clear
linktitle: Clear
articleTitle: Clear
second_title: Aspose.Words for .NET
description: 使用清除方法轻松清除结构化文档标签的内容，并显示定义的占位符以增强文档管理。
type: docs
weight: 360
url: /zh/net/aspose.words.markup/structureddocumenttag/clear/
---
## StructuredDocumentTag.Clear method

清除此结构化文档标签的内容，并显示占位符（如果已定义）。

```csharp
public void Clear()
```

## 评论

如果结构化文档标签有修订，则无法清除其内容。

如果此结构化文档标签映射到自定义 XML（使用[`XmlMapping`](../xmlmapping/) 属性），则引用的 XML 节点被清除。

## 例子

展示如何删除结构化文档标签元素的内容。

```csharp
Document doc = new Document();

// 创建一个纯文本结构化文档标签，然后将其附加到文档中。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Block);
doc.FirstSection.Body.AppendChild(tag);

// 这个结构化文档标签，以文本框的形式，已经显示了占位符文本。
Assert.AreEqual("Click here to enter text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// 创建包含文本内容的构建块。
GlossaryDocument glossaryDoc = doc.GlossaryDocument;
BuildingBlock substituteBlock = new BuildingBlock(glossaryDoc);
substituteBlock.Name = "My placeholder";
substituteBlock.AppendChild(new Section(glossaryDoc));
substituteBlock.FirstSection.EnsureMinimum();
substituteBlock.FirstSection.Body.FirstParagraph.AppendChild(new Run(glossaryDoc, "Custom placeholder text."));
glossaryDoc.AppendChild(substituteBlock);

// 将结构化文档标签的“PlaceholderName”属性设置为我们的构建块的名称以获取
// 结构化文档标签来显示构建块的内容来代替原始的默认文本。
tag.PlaceholderName = "My placeholder";

Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
Assert.True(tag.IsShowingPlaceholderText);

// 编辑结构化文档标签的文本并隐藏占位符文本。
Run run = (Run)tag.GetChild(NodeType.Run, 0, true);
run.Text = "New text.";
tag.IsShowingPlaceholderText = false;

Assert.AreEqual("New text.", tag.GetText().Trim());

// 使用“Clear”方法清除此结构化文档标签的内容并再次显示占位符。
tag.Clear();

Assert.True(tag.IsShowingPlaceholderText);
Assert.AreEqual("Custom placeholder text.", tag.GetText().Trim());
```

### 也可以看看

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
