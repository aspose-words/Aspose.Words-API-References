---
title: "Aspose::Words::SubDocument class"
linktitle: "SubDocument"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::SubDocument class. 表示一个 SubDocument —— 它是对外部存储文档的引用。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 66000
url: /zh/cpp/aspose.words/subdocument/
---
## SubDocument class


表示 **SubDocument** ——它是对外部存储文档的引用。要了解更多，请访问 [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) 文档文章。

```cpp
class SubDocument : public Aspose::Words::Node
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [Clone](../node/clone/)(bool) | 创建节点的副本。 |
| [get_CustomNodeId](../node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../node/get_document/)() const | 获取此节点所属的文档。 |
| virtual [get_IsComposite](../node/get_iscomposite/)() | 如果此节点可以包含其他节点，则返回 **true**。 |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [SubDocument](../nodetype/)。 |
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
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


在此版本的 Aspose.Words 中，[SubDocument](./) 节点不提供用于创建或修改子文档的公共方法和属性。在此版本中，您无法实例化 [SubDocument](./) 节点或修改现有节点，除非删除它们。

[SubDocument](./) can only be a child of [Paragraph](../paragraph/).

## 示例



展示如何访问主文档的子文档。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Master document.docx");

System::SharedPtr<Aspose::Words::NodeCollection> subDocuments = doc->GetChildNodes(Aspose::Words::NodeType::SubDocument, true);

// 此节点用作对外部文档的引用，其内容无法访问。
auto subDocument = System::ExplicitCast<Aspose::Words::SubDocument>(subDocuments->idx_get(0));

ASSERT_FALSE(subDocument->get_IsComposite());
```

## 另见

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
