---
title: "Aspose::Words::CommentRangeEnd class"
linktitle: "CommentRangeEnd"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::CommentRangeEnd 类。表示具有关联评论的文本区域的结束位置。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words/commentrangeend/
---
## CommentRangeEnd class


表示与评论关联的文本区域的结束。要了解更多信息，请访问 [Working with Comments](https://docs.aspose.com/words/cpp/working-with-comments/) 文档文章。

```cpp
class CommentRangeEnd : public Aspose::Words::Node,
                        public Aspose::Words::IDisplaceableByCustomXml,
                        public Aspose::Words::INodeWithAnnotationId
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [Clone](../node/clone/)(bool) | 创建节点的副本。 |
| [CommentRangeEnd](./commentrangeend/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, int32_t) | 初始化此类的新实例。 |
| [get_CustomNodeId](../node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../node/get_document/)() const | 获取此节点所属的文档。 |
| [get_Id](./get_id/)() const | 指定此区域关联的评论的标识符。 |
| virtual [get_IsComposite](../node/get_iscomposite/)() | 如果此节点可以包含其他节点，则返回 **true**。 |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [CommentRangeEnd](../nodetype/)。 |
| [get_ParentNode](../node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_PreviousSibling](../node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | 返回一个 [Range](../range/) 对象，表示此节点中包含的文档部分。 |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../nodetype/) 的第一个祖先。 |
| [GetAncestorOf](../node/getancestorof/)() |  |
| virtual [GetText](../node/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [PreviousPreOrder](../node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](../node/remove/)() | 从父节点中移除自身。 |
| [set_CustomNodeId](../node/set_customnodeid/)(int32_t) | 设置 [Aspose::Words::Node::get_CustomNodeId](../node/get_customnodeid/) 的值。 |
| [set_Id](./set_id/)(int32_t) | 指定此区域关联的评论的标识符。 |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


要创建锚定到文本区域的评论，您需要创建一个 [Comment](../comment/)，然后创建 [CommentRangeStart](../commentrangestart/) 和 [CommentRangeEnd](./)，并将它们的标识符设置为相同的 [Id](../comment/get_id/) 值。

[CommentRangeEnd](./) is an inline-level node and can only be a child of [Paragraph](../paragraph/).

## 另见

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
