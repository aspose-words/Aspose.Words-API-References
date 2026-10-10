---
title: "Aspose::Words::BookmarkEnd class"
linktitle: "BookmarkEnd"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::BookmarkEnd class。表示 Word 文档中书签的结束位置。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 5000
url: /zh/cpp/aspose.words/bookmarkend/
---
## BookmarkEnd class


表示 Word 文档中书签的结束位置。欲了解更多，请访问[书签使用指南](https://docs.aspose.com/words/cpp/working-with-bookmarks/)文档文章。

```cpp
class BookmarkEnd : public Aspose::Words::Node,
                    public Aspose::Words::IBookmarkNode,
                    public Aspose::Words::IDisplaceableByCustomXml
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [BookmarkEnd](./bookmarkend/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, const System::String\&) | 初始化 [BookmarkEnd](./) 类的新实例。 |
| [Clone](../node/clone/)(bool) | 创建节点的副本。 |
| [get_CustomNodeId](../node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../node/get_document/)() const | 获取此节点所属的文档。 |
| virtual [get_IsComposite](../node/get_iscomposite/)() | 如果此节点可以包含其他节点，则返回 **true**。 |
| [get_Name](./get_name/)() override | 获取书签名称。 |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [BookmarkEnd](../nodetype/)。 |
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
| [set_Name](./set_name/)(System::String) override | 设置书签名称。 |
| [set_NextNode](../node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [ToString](../node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |
## 备注


Word 文档中的完整书签由一个 [BookmarkStart](../bookmarkstart/) 和一个具有相同书签名称的匹配的 [BookmarkEnd](./) 组成。

[BookmarkStart](../bookmarkstart/) and [BookmarkEnd](./) are just markers inside a document that specify where the bookmark starts and ends.

使用 [Bookmark](../bookmark/) 类作为“外观”，将书签作为单个对象进行操作。
## 另见

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
