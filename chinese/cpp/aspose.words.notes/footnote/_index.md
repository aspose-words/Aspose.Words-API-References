---
title: "Aspose::Words::Notes::Footnote 类"
linktitle: "脚注"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::Footnote 类。表示脚注或尾注文本的容器。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.notes/footnote/
---
## Footnote class


表示脚注或尾注文本的容器。欲了解更多，请访问 [Working with Footnote and Endnote](https://docs.aspose.com/words/cpp/working-with-footnote-and-endnote/) 文档文章。

```cpp
class Footnote : public Aspose::Words::InlineStory,
                 public Aspose::Words::Revisions::ITrackableNode
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问脚注的结束位置。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问脚注的起始位置。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [EnsureMinimum](../../aspose.words/inlinestory/ensureminimum/)() | 如果最后一个子节点不是段落，则创建并追加一个空段落。 |
| [Footnote](./footnote/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, Aspose::Words::Notes::FootnoteType) | 初始化 [Footnote](./) 类的实例。 |
| [get_ActualReferenceMark](./get_actualreferencemark/)() | 获取此脚注在文档中显示的引用标记的实际文本。 |
| [get_Count](../../aspose.words/compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FirstParagraph](../../aspose.words/inlinestory/get_firstparagraph/)() override | 获取故事中的第一段落。 |
| [get_Font](../../aspose.words/inlinestory/get_font/)() | 提供对该对象锚字符字体格式的访问。 |
| [get_FootnoteType](./get_footnotetype/)() const | 返回一个值，指定这是脚注还是尾注。 |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_IsAuto](./get_isauto/)() const | 保存一个值，指定这是自动编号的脚注还是使用用户自定义引用标记的脚注。 |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_IsDeleteRevision](../../aspose.words/inlinestory/get_isdeleterevision/)() | 如果在启用更改跟踪的 Microsoft Word 中删除了此对象，则返回 true。 |
| [get_IsInsertRevision](../../aspose.words/inlinestory/get_isinsertrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中插入了此对象，则返回 true。 |
| [get_IsMoveFromRevision](../../aspose.words/inlinestory/get_ismovefromrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（删除）了此对象，则返回 **true**。 |
| [get_IsMoveToRevision](../../aspose.words/inlinestory/get_ismovetorevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（插入）了此对象，则返回 **true**。 |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_LastParagraph](../../aspose.words/inlinestory/get_lastparagraph/)() override | 获取故事中的最后一个段落。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [Footnote](../../aspose.words/nodetype/)。 |
| [get_Paragraphs](../../aspose.words/inlinestory/get_paragraphs/)() override | 获取作为故事直接子节点的段落集合。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_ParentParagraph](../../aspose.words/inlinestory/get_parentparagraph/)() | 检索此节点的父级 [Paragraph](../../aspose.words/paragraph/)。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [get_ReferenceMark](./get_referencemark/)() const | 获取/设置用于此脚注的自定义引用标记。默认值为 **empty string**，表示使用自动编号的脚注。 |
| [get_StoryType](./get_storytype/)() override | 返回 [Footnotes](../../aspose.words/storytype/) 或 [Endnotes](../../aspose.words/storytype/)。 |
| [get_Tables](../../aspose.words/inlinestory/get_tables/)() override | 获取作为故事直接子节点的表格集合。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../../aspose.words/nodetype/) 的第一个祖先节点。 |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | 返回匹配指定类型的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | 提供对该节点的子节点进行 foreach 样式迭代的支持。 |
| [GetText](../../aspose.words/compositenode/gettext/)() override | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [IndexOf](../../aspose.words/compositenode/indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 返回指定子节点在子节点数组中的索引。 |
| [InsertAfter](../../aspose.words/compositenode/insertafter/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [InsertBefore](../../aspose.words/compositenode/insertbefore/)(T, const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [PrependChild](../../aspose.words/compositenode/prependchild/)(T) |  |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 从父节点中移除自身。 |
| [RemoveAllChildren](../../aspose.words/compositenode/removeallchildren/)() | 移除当前节点的所有子节点。 |
| [RemoveChild](../../aspose.words/compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 移除当前节点的所有 [SmartTag](../../aspose.words.markup/smarttag/) 后代节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | 选择匹配 XPath 表达式的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | 选择第一个匹配 XPath 表达式的 [Node](../../aspose.words/node/)。 |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | 用于设置 [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) 的 setter。 |
| [set_IsAuto](./set_isauto/)(bool) | 用于 [Aspose::Words::Notes::Footnote::get_IsAuto](./get_isauto/) 的设置器。 |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ReferenceMark](./set_referencemark/)(const System::String\&) | 用于 [Aspose::Words::Notes::Footnote::get_ReferenceMark](./get_referencemark/) 的设置器。 |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


[Footnote](./) 类用于在 Word 文档中表示脚注和尾注。

[Footnote](./) is an inline-level node and can only be a child of [Paragraph](../../aspose.words/paragraph/).

[Footnote](./) can contain [Paragraph](../../aspose.words/paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

## 示例



展示如何插入和自定义脚注。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 添加文本，并用脚注引用它。此脚注将在文本后放置一个小的上标引用
// 标记在它引用的文本之后，并在页面底部的正文下方创建一个条目。
// 此条目将包含脚注的引用标记和引用文本，
// 我们将把它传递给文档生成器的 "InsertFootnote" 方法。
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// 如果此属性设置为 "true"，则我们的脚注引用标记
// 将是其在该节所有脚注中的索引。
// 这是第一个脚注，因此引用标记将是 "1"。
ASSERT_TRUE(footnote->get_IsAuto());

// 我们可以将文档生成器移动到脚注内部以编辑其引用文本。
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// 我们可以设置自定义引用标记，脚注将使用该标记而不是其索引号。
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// 将 "IsAuto" 标志设置为 true 的书签仍会显示其真实索引
// 即使之前的书签显示自定义引用标记，此书签的引用标记仍将是 "3"。
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```

## 另见

* Class [InlineStory](../../aspose.words/inlinestory/)
* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
