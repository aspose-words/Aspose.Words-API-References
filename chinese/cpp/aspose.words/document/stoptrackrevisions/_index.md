---
title: "Aspose::Words::Document::StopTrackRevisions 方法"
linktitle: "StopTrackRevisions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Document::StopTrackRevisions 方法。停止在 C++ 中自动将文档更改标记为修订。"
type: docs
weight: 93000
url: /zh/cpp/aspose.words/document/stoptrackrevisions/
---
## Document::StopTrackRevisions method


停止自动将文档更改标记为修订。

```cpp
void Aspose::Words::Document::StopTrackRevisions()
```


## 示例



展示如何在编辑文档时跟踪修订。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 编辑文档通常不会算作修订，除非我们开始跟踪它们。
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// 停止跟踪修订，以免将任何后续编辑计为修订。
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// 创建修订会为其分配操作的日期和时间。
// 当我们开始跟踪修订时，可以通过传递 DateTime.MinValue 来禁用此功能。
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// 我们可以通过编程方式接受/拒绝这些修订
// 例如调用 Document.AcceptAllRevisions 方法，或每个修订的 Accept 方法。
// 在 Microsoft Word 中，我们可以通过 “审阅” → “更改” 手动处理它们。
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## 另见

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
