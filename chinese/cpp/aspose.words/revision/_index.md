---
title: "Aspose::Words::Revision 类"
linktitle: "修订"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Revision 类。表示文档节点或样式中的修订（跟踪更改）。使用 RevisionType 检查此修订的类型。欲了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 52000
url: /zh/cpp/aspose.words/revision/
---
## Revision class


表示文档节点或样式中的修订（跟踪更改）。使用 [RevisionType](./get_revisiontype/) 检查此修订的类型。欲了解更多信息，请访问 [Track Changes in a Document](https://docs.aspose.com/words/cpp/track-changes-in-a-document/) 文档文章。

```cpp
class Revision : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [Accept](./accept/)() | 接受此修订。 |
| [get_Author](./get_author/)() | 获取或设置此修订的作者。不能为空字符串或 **null**。 |
| [get_DateTime](./get_datetime/)() | 获取或设置此修订的日期/时间。 |
| [get_Group](./get_group/)() | 获取修订组。如果修订不属于任何组，则返回 **null**。 |
| [get_ParentNode](./get_parentnode/)() | 获取此修订的直接父节点（所有者）。此属性适用于除 [StyleDefinitionChange](../revisiontype/) 之外的任何修订类型。 |
| [get_ParentStyle](./get_parentstyle/)() | 获取此修订的直接父样式（所有者）。此属性仅适用于 [StyleDefinitionChange](../revisiontype/) 修订类型。 |
| [get_RevisionType](./get_revisiontype/)() const | 获取此修订的类型。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Reject](./reject/)() | 拒绝此修订。 |
| [set_Author](./set_author/)(const System::String\&) | 用于 [Aspose::Words::Revision::get_Author](./get_author/) 的设置器。 |
| [set_DateTime](./set_datetime/)(System::DateTime) | 用于 [Aspose::Words::Revision::get_DateTime](./get_datetime/) 的设置器。 |
| static [Type](./type/)() |  |

## 示例



展示如何在文档中使用修订。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 对文档的普通编辑不计为修订。
builder->Write(u"This does not count as a revision. ");

ASSERT_FALSE(doc->get_HasRevisions());

// 要将我们的编辑登记为修订，需要声明作者，然后开始跟踪它们。
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

builder->Write(u"This is revision #1. ");

ASSERT_TRUE(doc->get_HasRevisions());
ASSERT_EQ(1, doc->get_Revisions()->get_Count());

// 此标志对应 Microsoft Word 中的 "Review" -> "Tracking" -> "Track Changes" 选项。
// “StartTrackRevisions” 方法不影响其值，
// 即使其值为 "false"，文档仍通过编程方式跟踪修订。
// 如果我们使用 Microsoft Word 打开此文档，它将不会跟踪修订。
ASSERT_FALSE(doc->get_TrackRevisions());

// 我们使用文档生成器添加了文本，因此第一个修订是插入类型的修订。
System::SharedPtr<Aspose::Words::Revision> revision = doc->get_Revisions()->idx_get(0);
ASSERT_EQ(u"John Doe", revision->get_Author());
ASSERT_EQ(u"This is revision #1. ", revision->get_ParentNode()->GetText());
ASSERT_EQ(Aspose::Words::RevisionType::Insertion, revision->get_RevisionType());
ASSERT_EQ(revision->get_DateTime().get_Date(), System::DateTime::get_Now().get_Date());
ASPOSE_ASSERT_EQ(doc->get_Revisions()->get_Groups()->idx_get(0), revision->get_Group());

// 删除一个 run 以创建删除类型的修订。
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->Remove();

// 添加新修订会将其放置在修订集合的开头。
ASSERT_EQ(Aspose::Words::RevisionType::Deletion, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(2, doc->get_Revisions()->get_Count());

// 插入修订会在文档正文中显示，即使在我们接受/拒绝修订之前。
// 拒绝修订将从正文中移除其节点。相反，构成删除修订的节点
// 也会在文档中保留，直到我们接受该修订。
ASSERT_EQ(u"This does not count as a revision. This is revision #1.", doc->GetText().Trim());

// 接受删除修订将从段落文本中移除其父节点
// 随后移除集合本身的修订。
doc->get_Revisions()->idx_get(0)->Accept();

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1.", doc->GetText().Trim());

builder->Writeln(u"");
builder->Write(u"This is revision #2.");

// 现在移动节点以创建移动类型的修订。
System::SharedPtr<Aspose::Words::Node> node = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1);
System::SharedPtr<Aspose::Words::Node> endNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_NextSibling();
System::SharedPtr<Aspose::Words::Node> referenceNode = doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0);

while (node != endNode)
{
    System::SharedPtr<Aspose::Words::Node> nextNode = node->get_NextSibling();
    doc->get_FirstSection()->get_Body()->InsertBefore<System::SharedPtr<Aspose::Words::Node>>(node, referenceNode);
    node = nextNode;
}

ASSERT_EQ(Aspose::Words::RevisionType::Moving, doc->get_Revisions()->idx_get(0)->get_RevisionType());
ASSERT_EQ(8, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #2.\rThis is revision #1. \rThis is revision #2.", doc->GetText().Trim());

// 移动修订现在位于索引 1。拒绝该修订以丢弃其内容。
doc->get_Revisions()->idx_get(1)->Reject();

ASSERT_EQ(6, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"This is revision #1. \rThis is revision #2.", doc->GetText().Trim());
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
