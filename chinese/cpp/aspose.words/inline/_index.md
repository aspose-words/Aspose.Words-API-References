---
title: "Aspose::Words::Inline 类"
linktitle: "Inline"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Inline 类。用于内联级节点的基类，这些节点可以关联字符格式，但不能拥有自己的子节点。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 36000
url: /zh/cpp/aspose.words/inline/
---
## Inline class


用于可以拥有字符格式但不能拥有子节点的内联级别节点的基类。要了解更多，请访问 [Logical Levels of Nodes in a Document](https://docs.aspose.com/words/cpp/logical-levels-of-nodes-in-a-document/) 文档文章。

```cpp
class Inline : public Aspose::Words::Node,
               public Aspose::Words::IInline,
               public Aspose::Words::Revisions::ITrackableNode
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [Accept](../node/accept/)(System::SharedPtr\<Aspose::Words::DocumentVisitor\>) | 接受访问者。 |
| [Clone](../node/clone/)(bool) | 创建节点的副本。 |
| [get_CustomNodeId](../node/get_customnodeid/)() const | 指定自定义节点标识符。 |
| virtual [get_Document](../node/get_document/)() const | 获取此节点所属的文档。 |
| [get_Font](./get_font/)() | 提供对该对象字体格式的访问。 |
| virtual [get_IsComposite](../node/get_iscomposite/)() | 如果此节点可以包含其他节点，则返回 **true**。 |
| [get_IsDeleteRevision](./get_isdeleterevision/)() | 如果在启用更改跟踪的 Microsoft Word 中删除了此对象，则返回 true。 |
| [get_IsFormatRevision](./get_isformatrevision/)() | 如果在启用更改跟踪时，Microsoft Word 中对象的格式被更改，则返回 true。 |
| [get_IsInsertRevision](./get_isinsertrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中插入了此对象，则返回 true。 |
| [get_IsMoveFromRevision](./get_ismovefromrevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（删除）了此对象，则返回 **true**。 |
| [get_IsMoveToRevision](./get_ismovetorevision/)() | 如果在启用更改跟踪的 Microsoft Word 中移动（插入）了此对象，则返回 **true**。 |
| [get_NextNode](../node/get_nextnode/)() const |  |
| [get_NextSibling](../node/get_nextsibling/)() | 获取紧随此节点之后的节点。 |
| virtual [get_NodeType](../node/get_nodetype/)() const | 获取此节点的类型。 |
| [get_ParentNode](../node/get_parentnode/)() | 获取此节点的直接父节点。 |
| [get_ParentParagraph](./get_parentparagraph/)() | 检索此节点的父级 [Paragraph](../paragraph/)。 |
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


从 [Inline](./) 派生的类可以是 [Paragraph](../paragraph/) 的子节点。

## 示例



展示如何确定内联节点的修订类型。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revision runs.docx");

// 当我们在文档中编辑时，如果通过 “审阅 -> 跟踪更改” 找到的 \"Track Changes\" 选项已开启，
// 在 Microsoft Word 中已打开时，我们所做的更改将计为修订。
// 使用 Aspose.Words 编辑文档时，我们可以通过以下方式开始跟踪修订：
// 调用文档的 \"StartTrackRevisions\" 方法开始，使用 \"StopTrackRevisions\" 方法停止跟踪。
// 我们可以接受修订，将其合并到文档中
// 或拒绝它们，以有效地撤销提议的更改。
ASSERT_EQ(6, doc->get_Revisions()->get_Count());

// 修订的父节点是该修订涉及的 Run。Run 是一种 Inline 节点。
auto run = System::ExplicitCast<Aspose::Words::Run>(doc->get_Revisions()->idx_get(0)->get_ParentNode());

System::SharedPtr<Aspose::Words::Paragraph> firstParagraph = run->get_ParentParagraph();
System::SharedPtr<Aspose::Words::RunCollection> runs = firstParagraph->get_Runs();

ASSERT_EQ(6, runs->ToArray()->get_Length());

// 以下是可以标记 Inline 节点的五种修订类型。
// 1 -  一个 \"insert\" 修订：
// 当我们在跟踪更改时插入文本时，会产生此修订。
ASSERT_TRUE(runs->idx_get(2)->get_IsInsertRevision());

// 2 -  一个 \"format\" 修订：
// 当我们在跟踪更改时更改文本的格式时，会产生此修订。
ASSERT_TRUE(runs->idx_get(2)->get_IsFormatRevision());

// 3 -  一个 \"move from\" 修订：
// 当我们在 Microsoft Word 中突出显示文本，然后将其拖动到文档的其他位置时
// 在跟踪更改时，会出现两个修订。
// \"move from\" 修订是我们移动之前原始文本的副本。
ASSERT_TRUE(runs->idx_get(4)->get_IsMoveFromRevision());

// 4 -  一个 \"move to\" 修订：
// \"move to\" 修订是我们在文档中新位置移动的文本。
// \"Move from\" 和 \"move to\" 修订在我们执行的每个移动修订中成对出现。
// 接受移动修订会删除 "move from" 修订及其文本，
// 并保留来自 "move to" 修订的文本。
// 拒绝移动修订则相反，会保留 "move from" 修订并删除 "move to" 修订。
ASSERT_TRUE(runs->idx_get(1)->get_IsMoveToRevision());

// 5 -  一个 "delete" 修订：
// 当我们在跟踪更改时删除文本时，会出现此修订。当我们这样删除文本时，
// 它会作为修订保留在文档中，直到我们接受该修订，
// 这将永久删除文本，或拒绝该修订，后者会保留我们删除的文本在原位置。
ASSERT_TRUE(runs->idx_get(5)->get_IsDeleteRevision());
```

## 另见

* Class [Node](../node/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
