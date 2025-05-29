---
title: Comment.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words for .NET
description: 探索 SetText 方法，这是一种用户友好的工具，可简化添加注释、增强工作流程并轻松提高工作效率。
type: docs
weight: 190
url: /zh/net/aspose.words/comment/settext/
---
## Comment.SetText method

这是一种便捷的方法，可以轻松设置评论的文本。

```csharp
public void SetText(string text)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| text | String | 评论的新文本。 |

## 评论

此方法允许快速从字符串设置评论文本。字符串可以包含段落分隔符，这将在评论中创建相应的文本段落。如果您想在评论中插入更复杂的元素，例如书签、表格或应用丰富的格式，则需要使用相应的节点类来构建评论文本。

## 例子

展示如何向文档添加评论，然后对其进行回复。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// 将注释放置在文档正文中的某个节点处。
// 此评论将显示在其段落的位置，
// 位于页面右侧边距之外，并用虚线将其与段落连接起来。
builder.CurrentParagraph.AppendChild(comment);

// 添加回复，它将显示在其父评论下。
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// 评论和回复都是评论节点。
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// 不回复其他评论的评论是“顶级”评论。它们没有祖先评论。
Assert.Null(comment.Ancestor);

// 回复有一个祖先顶级评论。
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### 也可以看看

* class [Comment](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
