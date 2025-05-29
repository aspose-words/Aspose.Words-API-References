---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: Aspose.Words for .NET
description: 使用 DocumentBuilder MoveToParagraph 方法轻松导航您的文档，使光标能够快速移动到您所在部分的任何段落。
type: docs
weight: 600
url: /zh/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

将光标移动到当前部分中的某个段落。

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| paragraphIndex | Int32 | 要移动到的段落的索引。 |
| characterIndex | Int32 | 段落内字符的索引。 负值表示从段落末尾开始的位置。使用 -1 表示移动到段落末尾。 |

## 评论

导航在当前章节的当前故事内进行。也就是说，如果您将光标移动到第一章节的主标题，那么*paragraphIndex*指定该部分的 header 内的段落的索引。

什么时候*paragraphIndex*大于或等于 0，表示从 开始的索引，其中 0 表示第一段。当*paragraphIndex*小于 0, 它指定了从该部分末尾开始的索引，其中 -1 表示最后一段。

## 例子

展示如何将构建器的光标位置移动到指定的段落。

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// 创建文档构建器来编辑文档。构建器的光标，
// 当我们调用它的文档构造方法时，它将在这里插入新节点，
// 当前位于文档的开头。
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// 将光标移动到不同的段落将把光标放在该段落的前面。
builder.MoveToParagraph(2, 0);
// 我们添加的任何新内容都将插入到该点。
builder.Writeln("This is a new third paragraph. ");
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
