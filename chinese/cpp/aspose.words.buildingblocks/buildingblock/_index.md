---
title: "Aspose::Words::BuildingBlocks::BuildingBlock class"
linktitle: "BuildingBlock"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BuildingBlocks::BuildingBlock 类。表示词汇文档条目，例如构建块、自动文本或自动更正条目。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words.buildingblocks/buildingblock/
---
## BuildingBlock class


表示词汇表文档条目，例如构建块、自动文本或自动更正条目。要了解更多信息，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class BuildingBlock : public Aspose::Words::CompositeNode
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问 [BuildingBlock](./) 的结束位置。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问 [BuildingBlock](./) 的起始位置。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [BuildingBlock](./buildingblock/)(const System::SharedPtr\<Aspose::Words::BuildingBlocks::GlossaryDocument\>\&) | 初始化此类的新实例。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [get_Behavior](./get_behavior/)() const | 指定在将构建块的内容插入主文档时应应用的行为。 |
| [get_Category](./get_category/)() const | 指定构建块的二级分类。 |
| [get_Count](../../aspose.words/compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| [get_Description](./get_description/)() const | 获取或设置与此构建块关联的描述。 |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FirstSection](./get_firstsection/)() | 获取构建块中的第一个节。 |
| [get_Gallery](./get_gallery/)() const | 指定构建块的一级分类，以用于分类或用户界面排序。 |
| [get_Guid](./get_guid/)() const | 获取或设置唯一标识此构建块的标识符（128 位 GUID）。 |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_LastSection](./get_lastsection/)() | 获取构建块中的最后一个节。 |
| [get_Name](./get_name/)() const | 获取或设置此构建块的名称。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [BuildingBlock](../../aspose.words/nodetype/) 值。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [get_Sections](./get_sections/)() | 返回表示构建块中所有节的集合。 |
| [get_Type](./get_type/)() const | 指定构建块类型。 |
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
| [set_Behavior](./set_behavior/)(Aspose::Words::BuildingBlocks::BuildingBlockBehavior) | 指定在将构建块的内容插入主文档时应应用的行为。 |
| [set_Category](./set_category/)(const System::String\&) | 用于设置 [Aspose::Words::BuildingBlocks::BuildingBlock::get_Category](./get_category/) 的 setter。 |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | 用于设置 [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) 的 setter。 |
| [set_Description](./set_description/)(const System::String\&) | 用于设置 [Aspose::Words::BuildingBlocks::BuildingBlock::get_Description](./get_description/) 的 setter。 |
| [set_Gallery](./set_gallery/)(Aspose::Words::BuildingBlocks::BuildingBlockGallery) | 用于设置 [Aspose::Words::BuildingBlocks::BuildingBlock::get_Gallery](./get_gallery/) 的 setter。 |
| [set_Guid](./set_guid/)(System::Guid) | 用于设置 [Aspose::Words::BuildingBlocks::BuildingBlock::get_Guid](./get_guid/) 的 setter。 |
| [set_Name](./set_name/)(const System::String\&) | 用于设置 [Aspose::Words::BuildingBlocks::BuildingBlock::get_Name](./get_name/) 的 setter。 |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Type](./set_type/)(Aspose::Words::BuildingBlocks::BuildingBlockType) | 用于设置 [Aspose::Words::BuildingBlocks::BuildingBlock::get_Type](./get_type/) 的 setter。 |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


[BuildingBlock](./) can contain only [Section](../../aspose.words/section/) nodes.

[BuildingBlock](./) can only be a child of [GlossaryDocument](../glossarydocument/).

您可以创建新的构建块并将其插入词汇文档。您可以修改或删除现有的构建块。您可以在文档之间复制或移动构建块。您可以将构建块的内容插入文档中。

对应于 OOXML 中的 **docPart**、**docPartPr** 和 **docPartBody** 元素。

## 另见

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
