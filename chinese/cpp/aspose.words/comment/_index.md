---
title: "Aspose::Words::Comment 类"
linktitle: "Comment"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Comment 类。表示评论文本的容器。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words/comment/
---
## Comment class


表示评论文本的容器。要了解更多信息，请访问 [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/) 文档文章。

```cpp
class Comment : public Aspose::Words::InlineStory,
                public Aspose::Words::INodeWithAnnotationId,
                public Aspose::Words::Revisions::IMoveTrackableNode
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问评论的结束位置。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问评论的起始位置。 |
| [AddReply](./addreply/)(const System::String\&, const System::String\&, System::DateTime, const System::String\&) | 向此评论添加回复。 |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | 创建节点的副本。 |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | 初始化 [Comment](./) 类的新实例。 |
| [Comment](./comment/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&, const System::String\&, System::DateTime) | 初始化 [Comment](./) 类的新实例。 |
| [EnsureMinimum](../inlinestory/ensureminimum/)() | 如果最后一个子节点不是段落，则创建并追加一个空段落。 |
| [get_Ancestor](./get_ancestor/)() | 返回父级 [Comment](./) 对象。对于顶层评论返回 **null**。 |
| [get_Author](./get_author/)() const | 获取或设置评论的作者名称。 |
| [get_Count](../compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| [get_DateTime](./get_datetime/)() const | 获取评论创建的日期和时间。 |
| [get_DateTimeUtc](./get_datetimeutc/)() | 获取评论创建的 UTC 日期和时间。 |
| virtual [get_Document](../node/get_document/)() const | 获取此节点所属的文档。 |
| [get_Done](./get_done/)() const | 获取或设置标记，指示评论已标记为完成。 |
| [get_FirstChild](../compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FirstParagraph](../inlinestory/get_firstparagraph/)() override | 获取故事中的第一段落。 |
| [get_Font](../inlinestory/get_font/)() | 提供对该对象锚字符字体格式的访问。 |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_Id](./get_id/)() const | 获取或设置评论标识符。 |
| [get_Initial](./get_initial/)() const | 获取或设置与特定评论关联的用户首字母缩写。 |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_IsDeleteRevision](../inlinestory/get_isdeleterevision/)() | 如果在启用更改跟踪的 Microsoft Word 中删除了此对象，则返回 true。 |
| [get_IsInsertRevision](../inlinestory/get_isinsertrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中插入了此对象，则返回 true。 |
| [get_IsMoveFromRevision](../inlinestory/get_ismovefromrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（删除）了此对象，则返回 **true**。 |
| [get_IsMoveToRevision](../inlinestory/get_ismovetorevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（插入）了此对象，则返回 **true**。 |
| [get_LastChild](../compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_LastParagraph](../inlinestory/get_lastparagraph/)() override | 获取故事中的最后一个段落。 |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [Comment](../nodetype/)。 |
| [get_Paragraphs](../inlinestory/get_paragraphs/)() override | 获取作为故事直接子节点的段落集合。 |
| [get_ParentId](./get_parentid/)() const | 获取父评论 ID。值为 **%-1** 表示该评论没有父级。 |
| [get_ParentNode](../node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_ParentParagraph](../inlinestory/get_parentparagraph/)() | 检索此节点的父级 [Paragraph](../paragraph/)。 |
| [get_PreviousSibling](../node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | 返回一个 [Range](../range/) 对象，表示此节点中包含的文档部分。 |
| [get_Replies](./get_replies/)() | 返回一个 [Comment](./) 对象集合，这些对象是指定评论的直接子评论。 |
| [get_StoryType](./get_storytype/)() override | 返回 [Comments](../storytype/)。 |
| [get_Tables](../inlinestory/get_tables/)() override | 获取作为故事直接子节点的表格集合。 |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../nodetype/) 的第一个祖先。 |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | 返回匹配指定类型的子节点的实时集合。 |
| [GetEnumerator](../compositenode/getenumerator/)() override | 提供对该节点的子节点进行 foreach 样式迭代的支持。 |
| [GetText](../compositenode/gettext/)() override | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定子节点在子节点数组中的索引。 |
| [InsertAfter](../compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [PrependChild](../compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](../node/remove/)() | 从父节点中移除自身。 |
| [RemoveAllChildren](../compositenode/removeallchildren/)() | 移除当前节点的所有子节点。 |
| [RemoveAllReplies](./removeallreplies/)() | 移除此评论的所有回复。 |
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveReply](./removereply/)(const System::SharedPtr\<Aspose::Words::Comment\>\&) | 移除对此评论的指定回复。 |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | 移除当前节点的所有 [SmartTag](../../aspose.words.markup/smarttag/) 后代节点。 |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | 选择匹配 XPath 表达式的节点列表。 |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | 选择匹配 XPath 表达式的第一个 [Node](../node/)。 |
| [set_Author](./set_author/)(const System::String\&) | [Aspose::Words::Comment::get_Author](./get_author/) 的设置器。 |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | 设置 [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) 的值。 |
| [set_DateTime](./set_datetime/)(System::DateTime) | 获取评论创建的日期和时间。 |
| [set_Done](./set_done/)(bool) | [Aspose::Words::Comment::get_Done](./get_done/) 的设置器。 |
| [set_Id](./set_id/)(int32_t) | [Aspose::Words::Comment::get_Id](./get_id/) 的设置器。 |
| [set_Initial](./set_initial/)(const System::String\&) | [Aspose::Words::Comment::get_Initial](./get_initial/) 的设置器。 |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ParentId](./set_parentid/)(int32_t) | 设置父评论 ID。值为 **%-1** 表示该评论没有父级。 |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SetText](./settext/)(const System::String\&) | 这是一个便利方法，允许轻松设置评论的文本。 |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


评论是一种注释，锚定在文本区域或文本位置。评论可以包含任意数量的块级内容。

如果一个 [Comment](./) 对象单独出现，评论将锚定在该 [Comment](./) 对象的位置。

要将评论锚定到文本区域，需要三个对象：[Comment](./)、[CommentRangeStart](../commentrangestart/) 和 [CommentRangeEnd](../commentrangeend/)。这三个对象必须共享相同的 [Id](./get_id/) 值。

[Comment](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

[Comment](./) can contain [Paragraph](../paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

## 示例



展示如何向文档添加评论，然后对其进行回复。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"My comment.");

// 将评论放置在文档正文中的节点上。
// 此评论将显示在其段落的位置，
// 位于页面右侧边距之外，并且有一条虚线将其连接到段落。
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// 添加一个回复，该回复将显示在其父评论下方。
comment->AddReply(u"Joe Bloggs", u"J.B.", System::DateTime::get_Now(), u"New reply");

// 评论和回复都是 Comment 节点。
ASSERT_EQ(2, doc->GetChildNodes(Aspose::Words::NodeType::Comment, true)->get_Count());

// 不回复其他评论的评论是“顶级”评论。它们没有上级评论。
ASSERT_TRUE(System::TestTools::IsNull(comment->get_Ancestor()));

// 回复拥有一个上级顶级评论。
ASPOSE_ASSERT_EQ(comment, comment->get_Replies()->idx_get(0)->get_Ancestor());

doc->Save(get_ArtifactsDir() + u"Comment.AddCommentWithReply.docx");
```


展示如何向段落添加评论。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// 在 Microsoft Word 中，我们可以右键单击文档正文中的此评论进行编辑或回复。
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## 另见

* Class [InlineStory](../inlinestory/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
