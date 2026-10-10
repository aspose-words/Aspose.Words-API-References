---
title: "Aspose::Words::DocumentBase 类"
linktitle: "DocumentBase"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::DocumentBase 类。提供 Word 文档的主文档和词汇表文档的抽象基类。要了解更多信息，请访问 C++ 中的文档文章。"
type: docs
weight: 21000
url: /zh/cpp/aspose.words/documentbase/
---
## DocumentBase class


为 Word 文档的主文档和词汇表文档提供抽象基类。要了解更多信息，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class DocumentBase : public Aspose::Words::CompositeNode
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | 接受访问者。 |
| virtual [AcceptEnd](../compositenode/acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | 当在派生类中实现时，调用指定文档访问器的 VisitXXXEnd 方法。 |
| virtual [AcceptStart](../compositenode/acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | 当在派生类中实现时，调用指定文档访问器的 VisitXXXStart 方法。 |
| [AppendChild](../compositenode/appendchild/)(T) |  |
| [Clone](../node/clone/)(bool) | 创建节点的副本。 |
| [get_BackgroundShape](./get_backgroundshape/)() const | 获取或设置文档的背景形状。可以为 **null**。 |
| [get_Count](../compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| [get_Document](./get_document/)() const override | 获取此实例。 |
| [get_FirstChild](../compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_FontInfos](./get_fontinfos/)() const | 提供对本文件中使用的字体属性的访问。 |
| [get_FootnoteSeparators](./get_footnoteseparators/)() const | 提供对文档中定义的脚注/尾注分隔符的访问。 |
| [get_HasChildNodes](../compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_IsComposite](../compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_LastChild](../compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_Lists](./get_lists/)() const | 提供对文档中使用的列表格式的访问。 |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeChangingCallback](./get_nodechangingcallback/)() | 当在文档中插入或删除节点时调用。 |
| virtual [get_NodeType](../node/get_nodetype/)() const | 获取此节点的类型。 |
| [get_PageColor](./get_pagecolor/)() | 获取或设置文档的页面颜色。此属性是 [BackgroundShape](./get_backgroundshape/) 的简化版本。 |
| [get_ParentNode](../node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_PreviousSibling](../node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | 返回一个 [Range](../range/) 对象，表示此节点中包含的文档部分。 |
| [get_ResourceLoadingCallback](./get_resourceloadingcallback/)() const | 允许控制外部资源的加载方式。 |
| [get_Styles](./get_styles/)() const | 返回文档中定义的样式集合。 |
| [get_WarningCallback](./get_warningcallback/)() const | 在各种文档处理过程中调用，当检测到可能导致数据或格式保真度丢失的问题时。 |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../nodetype/) 的第一个祖先。 |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetChild](../compositenode/getchild/)(Aspose::Words::NodeType, int32_t, bool) | 返回匹配指定类型的第 N 个子节点。 |
| [GetChildNodes](../compositenode/getchildnodes/)(Aspose::Words::NodeType, bool) | 返回匹配指定类型的子节点的实时集合。 |
| [GetEnumerator](../compositenode/getenumerator/)() override | 提供对该节点的子节点进行 foreach 样式迭代的支持。 |
| [GetText](../compositenode/gettext/)() override | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool) | 将另一个文档的节点导入到当前文档。 |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode) | 将节点从另一个文档导入到当前文档，并提供控制格式的选项。 |
| [ImportNode](./importnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&, bool, Aspose::Words::ImportFormatMode, const System::SharedPtr\<Aspose::Words::ImportFormatOptions\>\&) | 将节点从另一个文档导入到当前文档，并提供控制格式的选项。 |
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
| [RemoveChild](../compositenode/removechild/)(T) |  |
| [RemoveSmartTags](../compositenode/removesmarttags/)() | 移除当前节点的所有 [SmartTag](../../aspose.words.markup/smarttag/) 后代节点。 |
| [SelectNodes](../compositenode/selectnodes/)(const System::String\&) | 选择匹配 XPath 表达式的节点列表。 |
| [SelectSingleNode](../compositenode/selectsinglenode/)(const System::String\&) | 选择匹配 XPath 表达式的第一个 [Node](../node/)。 |
| [set_BackgroundShape](./set_backgroundshape/)(const System::SharedPtr\<Aspose::Words::Drawing::Shape\>\&) | 用于设置 [Aspose::Words::DocumentBase::get_BackgroundShape](./get_backgroundshape/) 的 setter。 |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | 设置 [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) 的值。 |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_NodeChangingCallback](./set_nodechangingcallback/)(const System::SharedPtr\<Aspose::Words::INodeChangingCallback\>\&) | 当在文档中插入或删除节点时调用。 |
| [set_PageColor](./set_pagecolor/)(System::Drawing::Color) | 用于设置 [Aspose::Words::DocumentBase::get_PageColor](./get_pagecolor/) 的 setter。 |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_ResourceLoadingCallback](./set_resourceloadingcallback/)(const System::SharedPtr\<Aspose::Words::Loading::IResourceLoadingCallback\>\&) | 允许控制外部资源的加载方式。 |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 用于设置 [Aspose::Words::DocumentBase::get_WarningCallback](./get_warningcallback/) 的 setter。 |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../compositenode/settemplateweakptr/)(uint32_t) override |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


Aspose.Words 将 Word 文档表示为节点树。[DocumentBase](./) 是树的根节点，包含文档的所有其他节点。

[DocumentBase](./) also stores document-wide information such as [Styles](./get_styles/) and [Lists](./get_lists/) that the tree nodes might refer to.

## 示例



展示如何初始化 [DocumentBase](./) 的子类。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(doc).get_BaseType());

auto glossaryDoc = System::MakeObject<Aspose::Words::BuildingBlocks::GlossaryDocument>();
doc->set_GlossaryDocument(glossaryDoc);

ASPOSE_ASSERT_EQ(System::ObjectExt::GetType<Aspose::Words::DocumentBase>(), System::ObjectExt::GetType(glossaryDoc).get_BaseType());
```

## 另见

* Class [CompositeNode](../compositenode/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
