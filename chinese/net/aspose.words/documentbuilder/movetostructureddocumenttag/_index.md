---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder MoveToStructuredDocumentTag 方法. 将光标移动到当前部分中的结构化文档标记 在 C#.
type: docs
weight: 580
url: /zh/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

将光标移动到当前部分中的结构化文档标记。

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | 要移动到的结构化文档标记的索引。 |
| characterIndex | Int32 | 结构化文档标记内的字符索引。 负值允许您指定从结构化文档标记末尾开始的位置。使用 -1 to 移动到结构化文档标记的末尾。如果结构化文档标记位于块级别，并且 您要将光标移动到其最后一段的末尾，请指定-2。 |

## 评论

导航在当前部分的当前故事内执行。也就是说，如果您将 光标移至第一部分的主标题，则*structuredDocumentTagIndex* 指定该部分的标头内结构化文档标记的索引。

什么时候*structuredDocumentTagIndex*大于或等于0，它指定从该部分的开头开始的index ，其中0是第一个结构化文档标记。当 *structuredDocumentTagIndex*小于 0，它指定从 the 部分末尾开始的索引，其中 -1 是最后一个结构化文档标记。

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

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

将光标移至结构化文档标签。

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | 要移动到的结构化文档标签。 |
| characterIndex | Int32 | 结构化文档标记内的字符索引。 负值允许您指定从结构化文档标记末尾开始的位置。使用 -1 to 移动到结构化文档标记的末尾。如果结构化文档标记位于块级别，并且 您要将光标移动到其最后一段的末尾，请指定-2。 |

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
