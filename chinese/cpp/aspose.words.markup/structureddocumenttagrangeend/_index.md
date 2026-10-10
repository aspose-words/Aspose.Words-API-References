---
title: "Aspose::Words::Markup::StructuredDocumentTagRangeEnd 类"
linktitle: "StructuredDocumentTagRangeEnd"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Markup::StructuredDocumentTagRangeEnd 类。表示接受多节内容的范围结构化文档标签的结束。另请参阅 StructuredDocumentTagRangeStart 节点。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.markup/structureddocumenttagrangeend/
---
## StructuredDocumentTagRangeEnd class


表示接受多节内容的 **ranged** 结构化文档标签的结束。另请参阅 [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/) 节点。要了解更多信息，请访问 [Structured Document Tags or Content Control](https://docs.aspose.com/words/cpp/working-with-content-control-sdt/) 文档文章。

```cpp
class StructuredDocumentTagRangeEnd : public Aspose::Words::Node
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) override | 接受访问者。 |
| [Clone](../../aspose.words/node/clone/)(bool) | 创建节点的副本。 |
| [get_CustomNodeId](../../aspose.words/node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../../aspose.words/node/get_document/)() const | 获取此节点所属的文档。 |
| [get_Id](./get_id/)() const | 为此 **StructuredDocumentTagRange** 节点指定唯一的只读持久数值 Id。对应的 [StructuredDocumentTagRangeStart](../structureddocumenttagrangestart/) 节点具有相同的 [Id](../structureddocumenttagrangestart/get_id/)。 |
| virtual [get_IsComposite](../../aspose.words/node/get_iscomposite/)() | 如果此节点可以包含其他节点，则返回 **true**。 |
| [get_NextNode](../../aspose.words/node/get_nextnode/)() const |  |
| [get_NextSibling](../../aspose.words/node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| [get_NodeType](./get_nodetype/)() const override | 返回 [StructuredDocumentTagRangeEnd](../../aspose.words/nodetype/)。 |
| [get_ParentNode](../../aspose.words/node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_PreviousSibling](../../aspose.words/node/get_previoussibling/)() | 获取紧挨此节点之前的节点。 |
| [get_PrevNode](../../aspose.words/node/get_prevnode/)() const |  |
| [get_Range](../../aspose.words/node/get_range/)() | 返回一个表示包含在此节点中的文档部分的 [Range](../../aspose.words/range/) 对象。 |
| [GetAncestor](../../aspose.words/node/getancestor/)(Aspose::Words::NodeType) | 获取指定 [NodeType](../../aspose.words/nodetype/) 的第一个祖先节点。 |
| [GetAncestorOf](../../aspose.words/node/getancestorof/)() |  |
| virtual [GetText](../../aspose.words/node/gettext/)() | 获取此节点及其所有子节点的文本。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsAncestorNode](../../aspose.words/node/isancestornode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [NextPreOrder](../../aspose.words/node/nextpreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取下一个节点。 |
| static [NodeTypeToString](../../aspose.words/node/nodetypetostring/)(Aspose::Words::NodeType) | 一个将节点类型枚举值转换为用户友好字符串的实用方法。 |
| [PreviousPreOrder](../../aspose.words/node/previouspreorder/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | 根据先序树遍历算法获取上一个节点。 |
| [Remove](../../aspose.words/node/remove/)() | 从父节点中移除自身。 |
| [set_CustomNodeId](../../aspose.words/node/set_customnodeid/)(int32_t) | 用于设置 [Aspose::Words::Node::get_CustomNodeId](../../aspose.words/node/get_customnodeid/) 的 setter。 |
| [set_NextNode](../../aspose.words/node/set_nextnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [set_PrevNode](../../aspose.words/node/set_prevnode/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [SetParent](../../aspose.words/node/setparent/)(const System::SharedPtr\<Aspose::Words::Node\>\&) |  |
| [StructuredDocumentTagRangeEnd](./structureddocumenttagrangeend/)(const System::SharedPtr\<Aspose::Words::DocumentBase\>\&, int32_t) | 初始化 **Structured document tag range end** 类的新实例。 |
| [ToString](../../aspose.words/node/tostring/)(Aspose::Words::SaveFormat) | 以指定格式将节点内容导出为字符串。 |
| [ToString](../../aspose.words/node/tostring/)(const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | 使用指定的保存选项将节点内容导出为字符串。 |
| static [Type](./type/)() |  |

## 示例



展示如何获取多节结构化文档标签的属性。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Multi-section structured document tags.docx");

auto rangeStartTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeStart>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeStart, true)->idx_get(0));
auto rangeEndTag = System::AsCast<Aspose::Words::Markup::StructuredDocumentTagRangeEnd>(doc->GetChildNodes(Aspose::Words::NodeType::StructuredDocumentTagRangeEnd, true)->idx_get(0));

std::cout << "StructuredDocumentTagRangeStart values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeStartTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|Title: {0}", rangeStartTag->get_Title()) << std::endl;
std::cout << System::String::Format(u"\t|PlaceholderName: {0}", rangeStartTag->get_PlaceholderName()) << std::endl;
std::cout << System::String::Format(u"\t|IsShowingPlaceholderText: {0}", rangeStartTag->get_IsShowingPlaceholderText()) << std::endl;
std::cout << System::String::Format(u"\t|LockContentControl: {0}", rangeStartTag->get_LockContentControl()) << std::endl;
std::cout << System::String::Format(u"\t|LockContents: {0}", rangeStartTag->get_LockContents()) << std::endl;
std::cout << System::String::Format(u"\t|Level: {0}", rangeStartTag->get_Level()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeStartTag->get_NodeType()) << std::endl;
std::cout << System::String::Format(u"\t|RangeEnd: {0}", rangeStartTag->get_RangeEnd()) << std::endl;
std::cout << System::String::Format(u"\t|Color: {0}", rangeStartTag->get_Color().ToArgb()) << std::endl;
std::cout << System::String::Format(u"\t|SdtType: {0}", rangeStartTag->get_SdtType()) << std::endl;
std::cout << System::String::Format(u"\t|FlatOpcContent: {0}", rangeStartTag->get_WordOpenXML()) << std::endl;
std::cout << System::String::Format(u"\t|Tag: {0}\n", rangeStartTag->get_Tag()) << std::endl;

std::cout << "StructuredDocumentTagRangeEnd values:" << std::endl;
std::cout << System::String::Format(u"\t|Id: {0}", rangeEndTag->get_Id()) << std::endl;
std::cout << System::String::Format(u"\t|NodeType: {0}", rangeEndTag->get_NodeType()) << std::endl;
```

## 另见

* Class [Node](../../aspose.words/node/)
* Namespace [Aspose::Words::Markup](../)
* Library [Aspose.Words for C++](../../)
