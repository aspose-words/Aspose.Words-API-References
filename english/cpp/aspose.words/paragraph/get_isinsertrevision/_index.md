---
title: Aspose::Words::Paragraph::get_IsInsertRevision method
linktitle: get_IsInsertRevision
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Paragraph::get_IsInsertRevision method. Returns true if this object was inserted in Microsoft Word while change tracking was enabled in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words/paragraph/get_isinsertrevision/
---
## Paragraph::get_IsInsertRevision method


Returns true if this object was inserted in Microsoft Word while change tracking was enabled.

```cpp
bool Aspose::Words::Paragraph::get_IsInsertRevision()
```


## Examples



Shows how to work with revision paragraphs. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();
System::SharedPtr<Aspose::Words::Paragraph> para = body->get_FirstParagraph();

para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Paragraph 1. "));
body->AppendParagraph(u"Paragraph 2. ");
body->AppendParagraph(u"Paragraph 3. ");

// The above paragraphs are not revisions.
// Paragraphs that we add after starting revision tracking will register as "Insert" revisions.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

para = body->AppendParagraph(u"Paragraph 4. ");

ASSERT_TRUE(para->get_IsInsertRevision());

// Paragraphs that we remove after starting revision tracking will register as "Delete" revisions.
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = body->get_Paragraphs();

ASSERT_EQ(4, paragraphs->get_Count());

para = paragraphs->idx_get(2);
para->Remove();

// Such paragraphs will remain until we either accept or reject the delete revision.
// Accepting the revision will remove the paragraph for good,
// and rejecting the revision will leave it in the document as if we never deleted it.
ASSERT_EQ(4, paragraphs->get_Count());
ASSERT_TRUE(para->get_IsDeleteRevision());

// Accept the revision, and then verify that the paragraph is gone.
doc->AcceptAllRevisions();

ASSERT_EQ(3, paragraphs->get_Count());
ASSERT_EQ(0, para->get_Count());
ASSERT_EQ(System::String(u"Paragraph 1. \r") + u"Paragraph 2. \r" + u"Paragraph 4.", doc->GetText().Trim());
```

## See Also

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
