---
title: "Aspose::Words::Notes::FootnoteSeparator 类"
linktitle: "FootnoteSeparator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Notes::FootnoteSeparator 类。表示文档中脚注/尾注分隔符及其后续内容的容器（C++）。"
type: docs
weight: 3334
url: /zh/cpp/aspose.words.notes/footnoteseparator/
---
## FootnoteSeparator class


表示文档中脚注/尾注分隔符和续接内容的容器。

```cpp
class FootnoteSeparator : public Aspose::Words::Story
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 当在派生类中实现时，调用指定文档访问器的 VisitXXXEnd 方法。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 当在派生类中实现时，调用指定文档访问器的 VisitXXXStart 方法。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [AppendParagraph](../../aspose.words/story/appendparagraph/)(const System::String\&) | 一个快捷方法，用于创建带可选文本的 [Paragraph](../../aspose.words/paragraph/) 对象，并将其追加到此对象的末尾。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [DeleteShapes](../../aspose.words/story/deleteshapes/)() | 删除此故事文本中的所有形状。 |
| [get_Count](../../aspose.words/compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FirstParagraph](../../aspose.words/story/get_firstparagraph/)() override | 获取故事中的第一段落。 |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_LastParagraph](../../aspose.words/story/get_lastparagraph/)() override | 获取故事中的最后一个段落。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 获取此节点的类型。 |
| [get_Paragraphs](../../aspose.words/story/get_paragraphs/)() override | 获取作为故事直接子节点的段落集合。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [get_SeparatorType](./get_separatortype/)() const |  |
| [get_StoryType](../../aspose.words/story/get_storytype/)() override | 获取此故事的类型。 |
| [get_Tables](../../aspose.words/story/get_tables/)() override | 获取作为故事直接子节点的表格集合。 |
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
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


[FootnoteSeparator](./) can contain [Paragraph](../../aspose.words/paragraph/) and [Table](../../aspose.words.tables/table/) child nodes.

在文档中，每种 [FootnoteSeparatorType](../footnoteseparatortype/) 只能有一个 [FootnoteSeparator](./)。

## 示例



展示如何管理脚注分隔符格式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// 对齐脚注分隔符。
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## 另见

* Class [Story](../../aspose.words/story/)
* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
