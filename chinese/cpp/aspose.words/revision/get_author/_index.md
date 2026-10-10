---
title: "Aspose::Words::Revision::get_Author 方法"
linktitle: "get_Author"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Revision::get_Author 方法。获取或设置此修订的作者。在 C++ 中不能为空字符串或 null。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words/revision/get_author/
---
## Revision::get_Author method


获取或设置此修订的作者。不能为空字符串或 **null**。

```cpp
System::String Aspose::Words::Revision::get_Author()
```


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

* Class [Revision](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
