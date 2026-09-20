---
title: "Aspose::Words::EditableRangeEnd class"
linktitle: "EditableRangeEnd"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::EditableRangeEnd 类。表示 Word 文档中可编辑范围的结束位置。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 25000
url: /zh/cpp/aspose.words/editablerangeend/
---
## EditableRangeEnd class


表示 Word 文档中可编辑范围的结束。要了解更多信息，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class EditableRangeEnd : public Aspose::Words::Node,
                         public Aspose::Words::IDisplaceableByCustomXml,
                         public Aspose::Words::INodeWithAnnotationId
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [Clone](../node/clone/)(bool) | 创建节点的副本。 |
| [get_CustomNodeId](../node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../node/get_document/)() const | 获取此节点所属的文档。 |
| [get_EditableRangeStart](./get_editablerangestart/)() | 对应的 [EditableRangeStart](../editablerangestart/)，通过 ID 获取。 |
| [get_Id](./get_id/)() const | 指定可编辑范围的标识符。 |
| virtual [get_IsComposite](../node/get_iscomposite/)() | 如果此节点可以包含其他节点，则返回 **true**。 |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [EditableRangeEnd](../nodetype/)。 |
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
| [set_Id](./set_id/)(int32_t) | 用于设置 [Aspose::Words::EditableRangeEnd::get_Id](./get_id/) 的 setter。 |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


Word 文档中的完整可编辑范围由一个 [EditableRangeStart](./get_editablerangestart/) 和一个具有相同 Id 的匹配的 [EditableRangeEnd](./) 组成。

[EditableRangeStart](./get_editablerangestart/) and [EditableRangeEnd](./) are just markers inside a document that specify where the editable range starts and ends.

使用 [EditableRange](../editablerange/) 类作为"facade"，将可编辑范围作为单个对象进行操作。


目前，仅在行内级别支持可编辑范围，即在 [Paragraph](../paragraph/) 内部，但可编辑范围的开始和结束可以位于不同的段落中。

## 另见

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
