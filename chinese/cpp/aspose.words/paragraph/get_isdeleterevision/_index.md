---
title: "Aspose::Words::Paragraph::get_IsDeleteRevision method"
linktitle: "get_IsDeleteRevision"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Paragraph::get_IsDeleteRevision 方法。若在启用更改跟踪的 Microsoft Word 中此对象被删除，则返回 true，使用 C++。"
type: docs
weight: 7000
url: /zh/cpp/aspose.words/paragraph/get_isdeleterevision/
---
## Paragraph::get_IsDeleteRevision method


如果在启用更改跟踪的 Microsoft Word 中删除了此对象，则返回 true。

```cpp
bool Aspose::Words::Paragraph::get_IsDeleteRevision()
```


## 示例



展示如何使用修订段落。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();
System::SharedPtr<Aspose::Words::Paragraph> para = body->get_FirstParagraph();

para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Paragraph 1. "));
body->AppendParagraph(u"Paragraph 2. ");
body->AppendParagraph(u"Paragraph 3. ");

// 上述段落不是修订。
// 在启动修订跟踪后添加的段落将被记录为 "Insert" 修订。
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

para = body->AppendParagraph(u"Paragraph 4. ");

ASSERT_TRUE(para->get_IsInsertRevision());

// 在启动修订跟踪后删除的段落将被记录为 "Delete" 修订。
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = body->get_Paragraphs();

ASSERT_EQ(4, paragraphs->get_Count());

para = paragraphs->idx_get(2);
para->Remove();

// 此类段落将保留，直到我们接受或拒绝删除修订。
// 接受修订将永久删除该段落，
// 而拒绝修订则会在文档中保留它，就好像我们从未删除过一样。
ASSERT_EQ(4, paragraphs->get_Count());
ASSERT_TRUE(para->get_IsDeleteRevision());

// 接受修订，然后验证该段落已消失。
doc->AcceptAllRevisions();

ASSERT_EQ(3, paragraphs->get_Count());
ASSERT_EQ(0, para->get_Count());
ASSERT_EQ(System::String(u"Paragraph 1. \r") + u"Paragraph 2. \r" + u"Paragraph 4.", doc->GetText().Trim());
```

## 另见

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
