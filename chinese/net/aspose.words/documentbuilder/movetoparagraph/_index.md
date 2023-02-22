---
title: DocumentBuilder.MoveToParagraph
second_title: Aspose.Words for .NET API 参考
description: DocumentBuilder 方法. 将光标移动到当前节中的段落
type: docs
weight: 540
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
| characterIndex | Int32 | 段落内字符的索引。 负值允许您指定从段落末尾开始的位置。使用 -1 移动到 段落的末尾。 |

### 评论

导航是在当前节的当前故事中执行的。 也就是说，如果您将光标移动到第一节的主标题， ，则段落索引指定该节的该标题 内的段落索引。

当paragraphIndex 大于或等于0 时，它指定一个从 开始的索引，0 是第一个段落。当paragraphIndex 小于0 时， 它指定从该节末尾开始的索引，-1 是最后一个段落。

### 例子

显示如何将构建器的光标位置移动到指定段落。

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// 创建文档构建器来编辑文档。建造者的光标，
// 这是当我们调用它的文档构造方法时它将插入新节点的点，
// 当前位于文档的开头。
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// 将该光标移动到不同的段落会将光标放在该段落的前面。
builder.MoveToParagraph(2, 0);
// 我们添加的任何新内容都将在该点插入。
builder.Writeln("This is a new third paragraph. ");
```

### 也可以看看

* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../documentbuilder/)
* 部件 [Aspose.Words](../../../)


