---
title: Comment Class
linktitle: Comment
articleTitle: Comment
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Comment 班级. 表示评论文本的容器 在 C#.
type: docs
weight: 230
url: /zh/net/aspose.words/comment/
---
## Comment class

表示评论文本的容器。

要了解更多信息，请访问[使用评论](https://docs.aspose.com/words/net/working-with-comments/)文档文章。

```csharp
public sealed class Comment : InlineStory
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Comment](comment/#constructor)(*[DocumentBase](../documentbase/)*) | 初始化一个新实例`Comment`类. |
| [Comment](comment/#constructor_1)(*[DocumentBase](../documentbase/), string, string, DateTime*) | 初始化一个新实例`Comment`类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | 返回父级`Comment`目的。退货`无效的`获取顶级评论。 |
| [Author](../../aspose.words/comment/author/) { get; set; } | 返回或设置评论的作者姓名。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直接子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | 获取发表评论的日期和时间。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取该节点所属的文档。 |
| [Done](../../aspose.words/comment/done/) { get; set; } | 获取或设置指示评论已标记为完成的标志。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | 获取故事中的第一段。 |
| [Font](../../aspose.words/inlinestory/font/) { get; } | 提供对此对象的锚字符的字体格式的访问。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果该节点有任何子节点. |
| [Id](../../aspose.words/comment/id/) { get; } | 获取评论标识符。 |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | 返回或设置与特定评论关联的用户的姓名缩写。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为该节点可以有子节点。 |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | 如果在启用更改跟踪时在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入到 Microsoft Word 中，则返回 true。 |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | 返回`真的`如果启用更改跟踪时在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | 获取故事的最后一段。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随该节点的下一个节点。 |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | 返回Comment. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | 获取故事直接子级的段落集合。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | 检索父级[`Paragraph`](../paragraph/)此节点的. |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取紧邻此节点之前的节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回一个[`Range`](../range/)表示此节点中包含的文档部分的对象。 |
| [Replies](../../aspose.words/comment/replies/) { get; } | 返回的集合`Comment`指定注释的直接子对象的对象。 |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | 返回Comments. |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | 获取作为故事的直接子级的表的集合。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客。 |
| [AddReply](../../aspose.words/comment/addreply/)(*string, string, DateTime, string*) | 添加对此评论的回复。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(*[Node](../node/)*) | 将指定节点添加到该节点的子节点列表的末尾。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | 如果最后一个子级不是段落，则创建并附加一个空段落。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点上的每个样式迭代提供支持。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(*[Node](../node/), [Node](../node/)*) | 在指定的引用节点之后立即插入指定的节点。 |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(*[Node](../node/), [Node](../node/)*) | 在指定的引用节点之前插入指定的节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | 根据先序树遍历算法获取下一个节点。 |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(*[Node](../node/)*) | 将指定节点添加到该节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | 根据先序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中删除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | 删除对此评论的所有回复。 |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(*[Node](../node/)*) | 删除指定的子节点。 |
| [RemoveReply](../../aspose.words/comment/removereply/)(*Comment*) | 删除对此评论的指定回复。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点. |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../node/)与 XPath 表达式匹配。 |
| [SetText](../../aspose.words/comment/settext/)(*string*) | 这是一种方便的方法，可以轻松设置评论文本。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点的内容导出到字符串中。 |

## 评论

注释是锚定到文本区域或文本中的位置的注释。 注释可以包含任意数量的块级内容。

如果一个`Comment`对象单独出现，注释锚定到 的位置`Comment`目的。

要将注释锚定到文本区域，需要三个对象：`Comment`, [`CommentRangeStart`](../commentrangestart/)和[`CommentRangeEnd`](../commentrangeend/) 。所有三个对象都需要共享相同的 [`Id`](./id/)价值。

`Comment`是一个内联级节点并且只能是[`Paragraph`](../paragraph/)。

`Comment`可以包含[`Paragraph`](../paragraph/)和[`Table`](../../aspose.words.tables/table/)子节点。

## 例子

演示如何向段落添加注释。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // 在Microsoft Word中，我们可以在文档正文中右键单击该注释进行编辑，或者回复。
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

演示如何向文档添加评论，然后回复它。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("My comment.");

// 将注释放置在文档正文中的节点处。
// 该注释将显示在其段落的位置，
// 页面右侧边距之外，并用虚线将其与其段落连接起来。
builder.CurrentParagraph.AppendChild(comment);

// 添加回复，该回复将显示在其父评论下方。
comment.AddReply("Joe Bloggs", "J.B.", DateTime.Now, "New reply");

// 评论和回复都是Comment节点。
Assert.AreEqual(2, doc.GetChildNodes(NodeType.Comment, true).Count);

// 不回复其他评论的评论是“顶级”。他们没有祖先的评论。
Assert.Null(comment.Ancestor);

// 回复有一个祖先顶级评论。
Assert.AreEqual(comment, comment.Replies[0].Ancestor);

doc.Save(ArtifactsDir + "Comment.AddCommentWithReply.docx");
```

### 也可以看看

* class [InlineStory](../inlinestory/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
