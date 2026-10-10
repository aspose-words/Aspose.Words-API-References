---
title: "Aspose::Words::BuildingBlocks::GlossaryDocument 类"
linktitle: "GlossaryDocument"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BuildingBlocks::GlossaryDocument 类。表示 Word 文档中词汇文档的根元素。词汇文档是 AutoText、AutoCorrect 条目和构建块的存储。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.buildingblocks/glossarydocument/
---
## GlossaryDocument class


表示 Word 文档中词汇表文档的根元素。词汇表文档是用于存储自动文本、自动更正条目和构建块的存储。要了解更多信息，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class GlossaryDocument : public Aspose::Words::DocumentBase
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问 Glossary 文档的结束位置。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问 Glossary 文档的起始位置。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [get_BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/)() const | 获取或设置文档的背景形状。可以为 **null**。 |
| [get_BuildingBlocks](./get_buildingblocks/)() | 返回一个类型化集合，表示词汇文档中的所有构建块。 |
| [get_Count](../../aspose.words/compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| [get_Document](../../aspose.words/documentbase/get_document/)() const override | 获取此实例。 |
| [get_FirstBuildingBlock](./get_firstbuildingblock/)() | 获取词汇文档中的第一个构建块。 |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FontInfos](../../aspose.words/documentbase/get_fontinfos/)() const | 提供对本文件中使用的字体属性的访问。 |
| [get_FootnoteSeparators](../../aspose.words/documentbase/get_footnoteseparators/)() const | 提供对文档中定义的脚注/尾注分隔符的访问。 |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_LastBuildingBlock](./get_lastbuildingblock/)() | 获取词汇文档中的最后一个构建块。 |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_Lists](../../aspose.words/documentbase/get_lists/)() const | 提供对文档中使用的列表格式的访问。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeChangingCallback](../../aspose.words/documentbase/get_nodechangingcallback/)() | 当在文档中插入或删除节点时调用。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [GlossaryDocument](../../aspose.words/nodetype/) 值。 |
| [get_PageColor](../../aspose.words/documentbase/get_pagecolor/)() | 获取或设置文档的页面颜色。此属性是 [BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/) 的简化版本。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [get_ResourceLoadingCallback](../../aspose.words/documentbase/get_resourceloadingcallback/)() const | 允许控制外部资源的加载方式。 |
| [get_Styles](../../aspose.words/documentbase/get_styles/)() const | 返回文档中定义的样式集合。 |
| [get_WarningCallback](../../aspose.words/documentbase/get_warningcallback/)() const | 在各种文档处理过程中调用，当检测到可能导致数据或格式保真度丢失的问题时。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../../aspose.words/nodetype/) 的第一个祖先节点。 |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetBuildingBlock](./getbuildingblock/)(Aspose::Words::BuildingBlocks::BuildingBlockGallery, const System::String\&, const System::String\&) | 使用指定的库、类别和名称查找构建块。 |
| [GetChild](../../aspose.words/compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../../aspose.words/compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | 返回匹配指定类型的子节点的实时集合。 |
| [GetEnumerator](../../aspose.words/compositenode/getenumerator/)() override | 提供对该节点的子节点进行 foreach 样式迭代的支持。 |
| [GetText](../../aspose.words/compositenode/gettext/)() override | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | 将另一个文档的节点导入到当前文档。 |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | 将节点从另一个文档导入到当前文档，并提供控制格式的选项。 |
| [ImportNode](../../aspose.words/documentbase/importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | 将节点从另一个文档导入到当前文档，并提供控制格式的选项。 |
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
| [set_BackgroundShape](../../aspose.words/documentbase/set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | [Aspose::Words::DocumentBase::get_BackgroundShape](../../aspose.words/documentbase/get_backgroundshape/) 的设置器。 |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | 用于设置 [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) 的 setter。 |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](../../aspose.words/documentbase/set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | 当在文档中插入或删除节点时调用。 |
| [set_PageColor](../../aspose.words/documentbase/set_pagecolor/)(System::Drawing::Color) | [Aspose::Words::DocumentBase::get_PageColor](../../aspose.words/documentbase/get_pagecolor/) 的设置器。 |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](../../aspose.words/documentbase/set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | 允许控制外部资源的加载方式。 |
| [set_WarningCallback](../../aspose.words/documentbase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | [Aspose::Words::DocumentBase::get_WarningCallback](../../aspose.words/documentbase/get_warningcallback/) 的设置器。 |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


某些文档（通常是模板）可以包含 AutoText、AutoCorrect 条目和/或 构建块（也称为 *glossary document entries*、*document parts* 或 *building blocks*）。

要访问构建块，需要将文档加载到 [Document](../../aspose.words/document/) 对象中。构建块可通过 [GlossaryDocument](../../aspose.words/document/get_glossarydocument/) 属性获取。

[GlossaryDocument](./) can contain any number of [BuildingBlock](../buildingblock/) objects. Each [BuildingBlock](../buildingblock/) represents one document part.

对应于 OOXML 中的 **glossaryDocument** 和 **docParts** 元素。

## 另见

* Class [DocumentBase](../../aspose.words/documentbase/)
* Namespace [Aspose::Words::BuildingBlocks](../)
* Library [Aspose.Words for C++](../../)
