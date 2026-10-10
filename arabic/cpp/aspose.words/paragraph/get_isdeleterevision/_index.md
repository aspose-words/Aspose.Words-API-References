---
title: "Aspose::Words::Paragraph::get_IsDeleteRevision method"
linktitle: "get_IsDeleteRevision"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Paragraph::get_IsDeleteRevision method. يرجع صحيح إذا تم حذف هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words/paragraph/get_isdeleterevision/
---
## Paragraph::get_IsDeleteRevision method


يرجع true إذا تم حذف هذا الكائن في Microsoft Word بينما كان تتبع التغييرات مفعلاً.

```cpp
bool Aspose::Words::Paragraph::get_IsDeleteRevision()
```


## أمثلة



يعرض كيفية العمل مع فقرات المراجعة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::Body> body = doc->get_FirstSection()->get_Body();
System::SharedPtr<Aspose::Words::Paragraph> para = body->get_FirstParagraph();

para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(System::MakeObject<Aspose::Words::Run>(doc, u"Paragraph 1. "));
body->AppendParagraph(u"Paragraph 2. ");
body->AppendParagraph(u"Paragraph 3. ");

// الفقرات أعلاه ليست مراجعات.
// الفقرات التي نضيفها بعد بدء تتبع المراجعات ستُسجل كـ "Insert" مراجعات.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());

para = body->AppendParagraph(u"Paragraph 4. ");

ASSERT_TRUE(para->get_IsInsertRevision());

// الفقرات التي نزيلها بعد بدء تتبع المراجعات ستُسجل كـ "Delete" مراجعات.
System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = body->get_Paragraphs();

ASSERT_EQ(4, paragraphs->get_Count());

para = paragraphs->idx_get(2);
para->Remove();

// ستبقى مثل هذه الفقرات حتى نقبل أو نرفض مراجعة الحذف.
// قبول المراجعة سيزيل الفقرة نهائيًا،
// ورفض المراجعة سيتركها في المستند كما لو لم نحذفها أبداً.
ASSERT_EQ(4, paragraphs->get_Count());
ASSERT_TRUE(para->get_IsDeleteRevision());

// اقبل المراجعة، ثم تحقق من أن الفقرة اختفت.
doc->AcceptAllRevisions();

ASSERT_EQ(3, paragraphs->get_Count());
ASSERT_EQ(0, para->get_Count());
ASSERT_EQ(System::String(u"Paragraph 1. \r") + u"Paragraph 2. \r" + u"Paragraph 4.", doc->GetText().Trim());
```

## انظر أيضًا

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
