---
title: get_IsDeleteRevision
second_title: Aspose.Words for C++ API Reference
description: Returns true if this object was deleted in Microsoft Word while change tracking was enabled.
type: docs
weight: 66
url: /cpp/aspose.words/paragraph/get_isdeleterevision/
---
## Paragraph.get_IsDeleteRevision method


Returns true if this object was deleted in Microsoft Word while change tracking was enabled.

```cpp
bool Aspose::Words::Paragraph::get_IsDeleteRevision()
```


## Examples




Shows how to work with revision paragraphs. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<Body> body = doc->get_FirstSection()->get_Body();
SharedPtr<Paragraph> para = body->get_FirstParagraph();

para->AppendChild(MakeObject<Run>(doc, u"Paragraph 1. "));
body->AppendParagraph(u"Paragraph 2. ");
body->AppendParagraph(u"Paragraph 3. ");

// The above paragraphs are not revisions.
// Paragraphs that we add after starting revision tracking will register as "Insert" revisions.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

para = body->AppendParagraph(u"Paragraph 4. ");

ASSERT_TRUE(para->get_IsInsertRevision());

// Paragraphs that we remove after starting revision tracking will register as "Delete" revisions.
SharedPtr<ParagraphCollection> paragraphs = body->get_Paragraphs();

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
ASSERT_EQ(String(u"Paragraph 1. \r") + u"Paragraph 2. \r" + u"Paragraph 4.", doc->GetText().Trim());
```

