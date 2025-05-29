---
title: Comment Class
linktitle: Comment
articleTitle: Comment
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Comment 类，这是您管理文档中注释文本的必备工具。通过无缝集成增强您的工作流程！
type: docs
weight: 420
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
| [Comment](comment/#constructor)(*[DocumentBase](../documentbase/)*) | 初始化`Comment`类. |
| [Comment](comment/#constructor_1)(*[DocumentBase](../documentbase/), string, string, DateTime*) | 初始化`Comment`类. |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Ancestor](../../aspose.words/comment/ancestor/) { get; } | 返回父级`Comment`对象。返回`无效的`用于顶级评论。 |
| [Author](../../aspose.words/comment/author/) { get; set; } | 返回或设置评论的作者姓名。 |
| [Count](../../aspose.words/compositenode/count/) { get; } | 获取此节点的直属子节点的数量。 |
| [CustomNodeId](../../aspose.words/node/customnodeid/) { get; set; } | 指定自定义节点标识符。 |
| [DateTime](../../aspose.words/comment/datetime/) { get; set; } | 获取发表评论的日期和时间。 |
| [DateTimeUtc](../../aspose.words/comment/datetimeutc/) { get; } | 获取发表评论的 UTC 日期和时间。 |
| virtual [Document](../../aspose.words/node/document/) { get; } | 获取此节点所属的文档。 |
| [Done](../../aspose.words/comment/done/) { get; set; } | 获取或设置标志，指示评论已被标记为完成。 |
| [FirstChild](../../aspose.words/compositenode/firstchild/) { get; } | 获取节点的第一个子节点。 |
| [FirstParagraph](../../aspose.words/inlinestory/firstparagraph/) { get; } | 获取故事的第一段。 |
| [Font](../../aspose.words/inlinestory/font/) { get; } | 提供对此对象的锚字符的字体格式的访问。 |
| [HasChildNodes](../../aspose.words/compositenode/haschildnodes/) { get; } | 返回`真的`如果此节点有任何子节点。 |
| [Id](../../aspose.words/comment/id/) { get; set; } | 获取或设置注释标识符。 |
| [Initial](../../aspose.words/comment/initial/) { get; set; } | 返回或设置与特定评论相关的用户的姓名首字母。 |
| override [IsComposite](../../aspose.words/compositenode/iscomposite/) { get; } | 返回`真的`因为这个节点可以有子节点。 |
| [IsDeleteRevision](../../aspose.words/inlinestory/isdeleterevision/) { get; } | 如果在启用更改跟踪的情况下在 Microsoft Word 中删除了此对象，则返回 true。 |
| [IsInsertRevision](../../aspose.words/inlinestory/isinsertrevision/) { get; } | 如果在启用更改跟踪的情况下将此对象插入 Microsoft Word，则返回 true。 |
| [IsMoveFromRevision](../../aspose.words/inlinestory/ismovefromrevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（删除）此对象。 |
| [IsMoveToRevision](../../aspose.words/inlinestory/ismovetorevision/) { get; } | 返回`真的`如果在启用更改跟踪的情况下在 Microsoft Word 中移动（插入）此对象。 |
| [LastChild](../../aspose.words/compositenode/lastchild/) { get; } | 获取节点的最后一个子节点。 |
| [LastParagraph](../../aspose.words/inlinestory/lastparagraph/) { get; } | 获取故事的最后一段。 |
| [NextSibling](../../aspose.words/node/nextsibling/) { get; } | 获取紧随此节点之后的节点。 |
| override [NodeType](../../aspose.words/comment/nodetype/) { get; } | 返回Comment. |
| [Paragraphs](../../aspose.words/inlinestory/paragraphs/) { get; } | 获取故事的直接子段落集合。 |
| [ParentId](../../aspose.words/comment/parentid/) { get; set; } | 获取或设置父评论 ID。值为`-1`表示该评论没有父评论。 |
| [ParentNode](../../aspose.words/node/parentnode/) { get; } | 获取此节点的直接父节点。 |
| [ParentParagraph](../../aspose.words/inlinestory/parentparagraph/) { get; } | 检索父级[`Paragraph`](../paragraph/)此节点的。 |
| [PreviousSibling](../../aspose.words/node/previoussibling/) { get; } | 获取此节点前一个节点。 |
| [Range](../../aspose.words/node/range/) { get; } | 返回[`Range`](../range/)表示此节点中包含的文档部分的对象。 |
| [Replies](../../aspose.words/comment/replies/) { get; } | 返回`Comment`指定注释的直接子对象。 |
| override [StoryType](../../aspose.words/comment/storytype/) { get; } | 返回Comments. |
| [Tables](../../aspose.words/inlinestory/tables/) { get; } | 获取故事的直接子表集合。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Accept](../../aspose.words/comment/accept/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客。 |
| override [AcceptEnd](../../aspose.words/comment/acceptend/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客访问评论末尾。 |
| override [AcceptStart](../../aspose.words/comment/acceptstart/)(*[DocumentVisitor](../documentvisitor/)*) | 接受访客访问评论的开头。 |
| [AddReply](../../aspose.words/comment/addreply/)(*string, string, DateTime, string*) | 添加对此评论的回复。 |
| [AppendChild&lt;T&gt;](../../aspose.words/compositenode/appendchild/)(*T*) | 将指定节点添加到此节点的子节点列表的末尾。 |
| [Clone](../../aspose.words/node/clone/)(*bool*) | 创建节点的副本。 |
| [CreateNavigator](../../aspose.words/compositenode/createnavigator/)() | 创建可用于遍历和读取节点的导航器。 |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | 如果最后一个子项不是段落，则创建并附加一个空段落。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(*[NodeType](../nodetype/)*) | 获取指定的第一个祖先[`NodeType`](../nodetype/). |
| [GetAncestor](../../aspose.words/node/getancestor/)(*Type*) | 获取指定对象类型的第一个祖先。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(*[NodeType](../nodetype/), int, bool*) | 返回与指定类型匹配的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(*[NodeType](../nodetype/), bool*) | 返回与指定类型匹配的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() | 为该节点的子节点提供对每个样式迭代的支持。 |
| override [GetText](../../aspose.words/compositenode/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [IndexOf](../../aspose.words/compositenode/indexof/)(*[Node](../node/)*) | 返回子节点数组中指定子节点的索引。 |
| [InsertAfter&lt;T&gt;](../../aspose.words/compositenode/insertafter/)(*T, [Node](../node/)*) | 在指定的参考节点后立即插入指定的节点。 |
| [InsertBefore&lt;T&gt;](../../aspose.words/compositenode/insertbefore/)(*T, [Node](../node/)*) | 在指定的参考节点之前立即插入指定的节点。 |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(*[Node](../node/)*) | 根据前序树遍历算法获取下一个节点。 |
| [PrependChild&lt;T&gt;](../../aspose.words/compositenode/prependchild/)(*T*) | 将指定节点添加到此节点的子节点列表的开头。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(*[Node](../node/)*) | 根据前序树遍历算法获取前一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 将自身从父级中移除。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 删除当前节点的所有子节点。 |
| [RemoveAllReplies](../../aspose.words/comment/removeallreplies/)() | 删除对此评论的所有回复。 |
| [RemoveChild&lt;T&gt;](../../aspose.words/compositenode/removechild/)(*T*) | 删除指定的子节点。 |
| [RemoveReply](../../aspose.words/comment/removereply/)(*Comment*) | 删除对此评论的指定回复。 |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 删除所有[`SmartTag`](../../aspose.words.markup/smarttag/)当前节点的后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(*string*) | 选择与 XPath 表达式匹配的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(*string*) | 选择第一个[`Node`](../node/)与 XPath 表达式匹配。 |
| [SetText](../../aspose.words/comment/settext/)(*string*) | 这是一种便捷的方法，可以轻松设置评论的文本。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveFormat](../saveformat/)*) | 将节点的内容导出为指定格式的字符串。 |
| [ToString](../../aspose.words/node/tostring/)(*[SaveOptions](../../aspose.words.saving/saveoptions/)*) | 使用指定的保存选项将节点内容导出为字符串。 |

## 评论

注释是锚定在文本区域或文本中某个位置的注解。 注释可以包含任意数量的块级内容。

如果`Comment`对象单独出现，注释锚定到 的位置`Comment`目的。

要将评论锚定到文本区域，需要三个对象：`Comment`, [`CommentRangeStart`](../commentrangestart/)和[`CommentRangeEnd`](../commentrangeend/) 。所有三个对象都需要共享相同的 [`Id`](./id/)价值。

`Comment`是内联级节点，并且只能是[`Paragraph`](../paragraph/)。

`Comment`可以包含[`Paragraph`](../paragraph/)和[`Table`](../../aspose.words.tables/table/)子节点。

## 例子

展示如何向段落添加注释。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

 // 在Microsoft Word中，我们可以在文档正文中右键单击该注释来编辑它，或者回复它。
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

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

* class [InlineStory](../inlinestory/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
