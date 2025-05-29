---
title: DocumentBuilder.MoveToStructuredDocumentTag
linktitle: MoveToStructuredDocumentTag
articleTitle: MoveToStructuredDocumentTag
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder MoveToStructuredDocumentTag 方法轻松导航到结构化文档标签，提高文档编辑效率。
type: docs
weight: 620
url: /zh/net/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## MoveToStructuredDocumentTag(*int, int*) {#movetostructureddocumenttag_1}

将光标移动到当前部分的结构化文档标签。

```csharp
public void MoveToStructuredDocumentTag(int structuredDocumentTagIndex, int characterIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| structuredDocumentTagIndex | Int32 | 要移动到的结构化文档标签的索引。 |
| characterIndex | Int32 | 结构化文档标签内字符的索引。 负值允许您指定从结构化文档标签末尾开始的位置。使用 -1 表示将光标移动到结构化文档标签的末尾。如果结构化文档标签位于块级别，并且 您希望将光标移动到其最后一段的末尾，请指定 -2。 |

## 评论

导航在当前章节的当前文章内进行。也就是说，如果您将 the 光标移动到第一章节的主标题，则*structuredDocumentTagIndex* 指定了该部分标题内的结构化文档标签的索引。

什么时候*structuredDocumentTagIndex*大于或等于 0，它指定从节的开头开始的 index ，其中 0 是第一个结构化文档标签。当 *structuredDocumentTagIndex*小于 0，它指定了从 部分末尾开始的索引，其中 -1 是最后一个结构化文档标签。

## 例子

展示如何在结构化文档标签内移动 DocumentBuilder 的光标。

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// 有几种方法可以移动光标：
// 1 - 通过索引移动到结构化文档标签的第一个字符。
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - 通过对象移动到结构化文档标签的第一个字符。
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - 移动到第二个结构化文档标签的末尾。
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);

// 获取当前选定的结构化文档标签。
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## MoveToStructuredDocumentTag(*[StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), int*) {#movetostructureddocumenttag}

将光标移动到结构化文档标签。

```csharp
public void MoveToStructuredDocumentTag(StructuredDocumentTag structuredDocumentTag, 
    int characterIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| structuredDocumentTag | StructuredDocumentTag | 要移动到的结构化文档标签。 |
| characterIndex | Int32 | 结构化文档标签内字符的索引。 负值允许您指定从结构化文档标签末尾开始的位置。使用 -1 表示将光标移动到结构化文档标签的末尾。如果结构化文档标签位于块级别，并且 您希望将光标移动到其最后一段的末尾，请指定 -2。 |

## 例子

展示如何在结构化文档标签内移动 DocumentBuilder 的光标。

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");
DocumentBuilder builder = new DocumentBuilder(doc);

// 有几种方法可以移动光标：
// 1 - 通过索引移动到结构化文档标签的第一个字符。
builder.MoveToStructuredDocumentTag(1, 1);

// 2 - 通过对象移动到结构化文档标签的第一个字符。
StructuredDocumentTag tag = (StructuredDocumentTag)doc.GetChild(NodeType.StructuredDocumentTag, 2, true);
builder.MoveToStructuredDocumentTag(tag, 1);
builder.Write(" New text.");

Assert.AreEqual("R New text.ichText", tag.GetText().Trim());

// 3 - 移动到第二个结构化文档标签的末尾。
builder.MoveToStructuredDocumentTag(1, -1);
Assert.True(builder.IsAtEndOfStructuredDocumentTag);

// 获取当前选定的结构化文档标签。
builder.CurrentStructuredDocumentTag.Color = Color.Green;

doc.Save(ArtifactsDir + "Document.MoveToStructuredDocumentTag.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
