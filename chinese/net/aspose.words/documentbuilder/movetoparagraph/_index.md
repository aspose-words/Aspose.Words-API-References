---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder MoveToParagraph 方法. 将光标移动到当前节中的段落 在 C#.
type: docs
weight: 560
url: /zh/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

将光标移动到当前节中的段落。

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| paragraphIndex | Int32 | 要移动到的段落的索引。 |
| characterIndex | Int32 | 段落内字符的索引。 负值允许您指定从段落末尾开始的位置。使用 -1 移至段落末尾 of 。 |

## 评论

导航在当前章节的当前故事内执行。 也就是说，如果您将光标移至第一章节的主标题， 那么*paragraphIndex*指定该节的 header 内段落的索引。

什么时候*paragraphIndex*大于或等于 0，它指定索引 from 节的开头，其中 0 为第一段。什么时候*paragraphIndex*小于 0， 它指定从该节末尾开始的索引，-1 是最后一段。

## 例子

演示如何将构建器的光标位置移动到指定段落。

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// 创建文档生成器来编辑文档。建造者的光标，
// 当我们调用它的文档构造方法时，它将插入新节点，
// 当前位于文档的开头。
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// 将光标移动到不同的段落会将光标置于该段落的前面。
builder.MoveToParagraph(2, 0);
// 我们添加的任何新内容都将在此时插入。
builder.Writeln("This is a new third paragraph. ");
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
