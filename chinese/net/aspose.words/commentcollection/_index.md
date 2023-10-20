---
title: CommentCollection Class
linktitle: CommentCollection
articleTitle: CommentCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.CommentCollection 班级. 提供对集合的类型化访问Comment节点 在 C#.
type: docs
weight: 240
url: /zh/net/aspose.words/commentcollection/
---
## CommentCollection class

提供对集合的类型化访问[`Comment`](../comment/)节点.

要了解更多信息，请访问[使用评论](https://docs.aspose.com/words/net/working-with-comments/)文档文章。

```csharp
public class CommentCollection : NodeCollection
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | 获取集合中的节点数。 |
| [Item](../../aspose.words/commentcollection/item/) { get; } | 检索[`Comment`](../comment/)在给定的索引. (2 indexers) |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | 将节点添加到集合的末尾。 |
| [Clear](../../aspose.words/nodecollection/clear/)() | 从此集合和文档中删除所有节点。 |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | 确定节点是否在集合中。 |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | 在节点集合上提供简单的“foreach”样式迭代。 |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | 返回指定节点的从零开始的索引。 |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | 将节点插入集合中指定索引处。 |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | 从集合和文档中删除节点。 |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | 从集合和文档中删除指定索引处的节点。 |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | 将集合中的所有节点复制到新的节点数组。 |

## 例子

展示如何将评论标记为“完成”。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

 // 插入注释以指出错误。
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

 // 注释有一个“Done”标志，默认设置为“false”。
// 如果评论建议我们在文档中进行更改，
// 我们可以应用更改，然后还设置“完成”标志以指示更正。
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// “完成”的注释将使其与众不同
// 来自那些未“完成”并带有褪色文本颜色的内容。
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### 也可以看看

* class [NodeCollection](../nodecollection/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
