---
title: "Aspose::Words::Markup::SmartTag class"
linktitle: "SmartTag"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::SmartTag 类。此元素指定段落中一个或多个内联结构（运行、图像、字段等）周围的智能标签的存在。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.markup/smarttag/
---
## SmartTag class


此元素指定段落中一个或多个内联结构（运行、图像、字段等）周围的智能标签的存在。了解更多，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。

```cpp
class SmartTag : public Aspose::Words::CompositeNode,
                 public Aspose::Words::Markup::IMarkupNode
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [AcceptEnd](./acceptend/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问 [SmartTag](./) 的结束位置。 |
| [AcceptStart](./acceptstart/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者以访问 [SmartTag](./) 的起始位置。 |
| [AppendChild](../../aspose.words/compositenode/appendchild/)(T) |  |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [get_Count](../../aspose.words/compositenode/get_count/)() | 获取此节点的直接子节点数量。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_Element](./get_element/)() const | 指定文档中智能标签的名称。 |
| [get_FirstChild](../../aspose.words/compositenode/get_firstchild/)() const | 获取节点的第一个子节点。 |
| [get_HasChildNodes](../../aspose.words/compositenode/get_haschildnodes/)() | 如果此节点有任何子节点，则返回 **true**。 |
| [get_IsComposite](../../aspose.words/compositenode/get_iscomposite/)() override | 因为此节点可以拥有子节点，返回 **true**。 |
| [get_LastChild](../../aspose.words/compositenode/get_lastchild/)() const | 获取节点的最后一个子节点。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [SmartTag](../../aspose.words/nodetype/)。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Properties](./get_properties/)() const | 智能标签属性的集合。 |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [get_Uri](./get_uri/)() const | 指定智能标签的命名空间 URI。 |
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
| [RemoveSmartTags](../../aspose.words/compositenode/removesmarttags/)() | 移除当前节点的所有 [SmartTag](./) 子孙节点。 |
| [SelectNodes](../../aspose.words/compositenode/selectnodes/)(const System::String\&) | 选择匹配 XPath 表达式的节点列表。 |
| [SelectSingleNode](../../aspose.words/compositenode/selectsinglenode/)(const System::String\&) | 选择第一个匹配 XPath 表达式的 [Node](../../aspose.words/node/)。 |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | 用于设置 [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) 的 setter。 |
| [set_Element](./set_element/)(const System::String\&) | 用于设置 [Aspose::Words::Markup::SmartTag::get_Element](./get_element/) 的 setter。 |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_Uri](./set_uri/)(const System::String\&) | 用于设置 [Aspose::Words::Markup::SmartTag::get_Uri](./get_uri/) 的 setter。 |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetTemplateWeakPtr](../../aspose.words/compositenode/settemplateweakptr/)(uint32_t) override |  |
| [SmartTag](./smarttag/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&) | 初始化 [SmartTag](./) 类的新实例。 |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


智能标签是一种自定义 XML 标记。智能标签通过为文档中的运行或一组运行提供基本的命名空间/名称，提供将客户定义的语义嵌入文档的功能。

[SmartTag](./) can be a child of a [Paragraph](../../aspose.words/paragraph/) or another [SmartTag](./) node.

智能标签内部可能出现的子节点完整列表包括 [BookmarkStart](../../aspose.words/bookmarkstart/)、[BookmarkEnd](../../aspose.words/bookmarkend/)、[FieldStart](../../aspose.words.fields/fieldstart/)、[FieldSeparator](../../aspose.words.fields/fieldseparator/)、[FieldEnd](../../aspose.words.fields/fieldend/)、[FormField](../../aspose.words.fields/formfield/)、[Comment](../../aspose.words/comment/)、[Footnote](../../aspose.words.notes/footnote/)、[Run](../../aspose.words/run/)、[SpecialChar](../../aspose.words/specialchar/)、[Shape](../../aspose.words.drawing/shape/)、[GroupShape](../../aspose.words.drawing/groupshape/)、[CommentRangeStart](../../aspose.words/commentrangestart/)、[CommentRangeEnd](../../aspose.words/commentrangeend/)、[SmartTag](./)。
## 另见

* Class [CompositeNode](../../aspose.words/compositenode/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
