---
title: "Aspose::Words::Fields::FieldSeparator 类"
linktitle: "FieldSeparator"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::FieldSeparator 类。表示 Word 字段分隔符，用于将字段代码与字段结果分开。了解更多，请访问 C++ 文档文章。"
type: docs
weight: 90000
url: /zh/cpp/aspose.words.fields/fieldseparator/
---
## FieldSeparator class


表示 Word 字段分隔符，用于将字段代码与字段结果分开。要了解更多，请访问 [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) 文档文章。

```cpp
class FieldSeparator : public Aspose::Words::Fields::FieldChar
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_FieldType](../fieldchar/get_fieldtype/)() const | 返回字段的类型。 |
| [get_Font](../../aspose.words/inline/get_font/)() | 提供对该对象字体格式的访问。 |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | 如果此节点可以包含其他节点，则返回 **true**。 |
| [get_IsDeleteRevision](../../aspose.words/inline/get_isdeleterevision/)() | 如果在启用更改跟踪的 Microsoft Word 中删除了此对象，则返回 true。 |
| [get_IsDirty](../fieldchar/get_isdirty/)() const | 获取或设置字段的当前结果是否因对文档的其他修改而不再正确（已过时）。 |
| [get_IsFormatRevision](../../aspose.words/inline/get_isformatrevision/)() | 如果在启用更改跟踪时，Microsoft Word 中对象的格式被更改，则返回 true。 |
| [get_IsInsertRevision](../../aspose.words/inline/get_isinsertrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中插入了此对象，则返回 true。 |
| [get_IsLocked](../fieldchar/get_islocked/)() const | 获取或设置父字段是否被锁定（不应重新计算其结果）。 |
| [get_IsMoveFromRevision](../../aspose.words/inline/get_ismovefromrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（删除）了此对象，则返回 **true**。 |
| [get_IsMoveToRevision](../../aspose.words/inline/get_ismovetorevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（插入）了此对象，则返回 **true**。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [FieldSeparator](../../aspose.words/nodetype/)。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_ParentParagraph](../../aspose.words/inline/get_parentparagraph/)() | 检索此节点的父级 [Paragraph](../../aspose.words/paragraph/)。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../../aspose.words/nodetype/) 的第一个祖先节点。 |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| [GetField](../fieldchar/getfield/)() | 返回字段字符对应的字段。 |
| [GetText](../../aspose.words/specialchar/gettext/)() override | 获取此节点表示的特殊字符。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 从父节点中移除自身。 |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | 用于设置 [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) 的 setter。 |
| [set_IsDirty](../fieldchar/set_isdirty/)(bool) | 用于 [Aspose::Words::Fields::FieldChar::get_IsDirty](../fieldchar/get_isdirty/) 的 setter。 |
| [set_IsLocked](../fieldchar/set_islocked/)(bool) | 用于 [Aspose::Words::Fields::FieldChar::get_IsLocked](../fieldchar/get_islocked/) 的 setter。 |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


[FieldSeparator](./) is an inline-level node and represented by the [FieldSeparatorChar](../../aspose.words/controlchar/fieldseparatorchar/) control character in the document.

[FieldSeparator](./) can only be a child of [Paragraph](../../aspose.words/paragraph/).

Microsoft Word 文档中的完整字段是一个复杂结构，由字段起始字符、字段代码、字段分隔符字符、字段结果和字段结束字符组成。有些字段仅包含字段起始、字段代码和字段结束。

要轻松在文档中插入新字段，请使用 [InsertField()](../) 方法。
## 另见

* Class [FieldChar](../fieldchar/)
* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
