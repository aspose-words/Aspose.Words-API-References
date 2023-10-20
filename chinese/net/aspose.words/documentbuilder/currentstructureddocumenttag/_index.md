---
title: DocumentBuilder.CurrentStructuredDocumentTag
linktitle: CurrentStructuredDocumentTag
articleTitle: CurrentStructuredDocumentTag
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder CurrentStructuredDocumentTag 财产. 获取当前在此选择的结构化文档标签DocumentBuilder 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words/documentbuilder/currentstructureddocumenttag/
---
## DocumentBuilder.CurrentStructuredDocumentTag property

获取当前在此选择的结构化文档标签[`DocumentBuilder`](../).

```csharp
public StructuredDocumentTag CurrentStructuredDocumentTag { get; }
```

## 例子

演示如何在结构化文档标签内移动 DocumentBuilder 的光标。

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// 移动光标有多种方法：
// 1 - 按索引移至结构化文档标记的第一个字符。
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - 按对象移动到结构化文档标记的第一个字符。
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - 移动到第二个结构化文档标记的末尾。
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);            

// 获取当前选择的结构化文档标签。
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
