---
title: "Aspose::Words::AbsolutePositionTab 类"
linktitle: "AbsolutePositionTab"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AbsolutePositionTab 类。绝对位置制表符是一种字符，用于在显示此 WordprocessingML 内容时在当前文本行上前进位置。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 1000
url: /zh/cpp/aspose.words/absolutepositiontab/
---
## AbsolutePositionTab class


绝对定位制表符是一种字符，用于在显示此 WordprocessingML 内容时在当前文本行上前进位置。欲了解更多，请访问[Aspose.Words 文档对象模型 (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/)文档文章。

```cpp
class AbsolutePositionTab : public Aspose::Words::SpecialChar
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [Clone](../node/clone/)(bool) | 创建节点的副本。 |
| [get_CustomNodeId](../node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../node/get_document/)() const | 获取此节点所属的文档。 |
| [get_Font](../inline/get_font/)() | 提供对该对象字体格式的访问。 |
| virtual [get_IsComposite](../node/get_iscomposite/)() | 如果此节点可以包含其他节点，则返回 **true**。 |
| [get_IsDeleteRevision](../inline/get_isdeleterevision/)() | 如果在启用更改跟踪的 Microsoft Word 中删除了此对象，则返回 true。 |
| [get_IsFormatRevision](../inline/get_isformatrevision/)() | 如果在启用更改跟踪时，Microsoft Word 中对象的格式被更改，则返回 true。 |
| [get_IsInsertRevision](../inline/get_isinsertrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中插入了此对象，则返回 true。 |
| [get_IsMoveFromRevision](../inline/get_ismovefromrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（删除）了此对象，则返回 **true**。 |
| [get_IsMoveToRevision](../inline/get_ismovetorevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（插入）了此对象，则返回 **true**。 |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](../specialchar/get_nodetype/)() const override | 返回 [SpecialChar](../nodetype/)。 |
| [get_ParentNode](../node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_ParentParagraph](../inline/get_parentparagraph/)() | 检索此节点的父级 [Paragraph](../paragraph/)。 |
| [get_PreviousSibling](../node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../node/get_prevnode/)() const |  |
| [get_Range](../node/get_range/)() | 返回一个 [Range](../range/) 对象，表示此节点中包含的文档部分。 |
| [GetAncestor](../node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../nodetype/) 的第一个祖先。 |
| [GetAncestorOf](../node/getancestorof/)() |  |
| [GetText](../specialchar/gettext/)() override | 获取此节点表示的特殊字符。 |
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
## 另见

* Class [SpecialChar](../specialchar/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
