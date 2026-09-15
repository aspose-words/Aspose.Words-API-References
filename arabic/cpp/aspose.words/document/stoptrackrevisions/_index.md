---
title: "Aspose::Words::Document::StopTrackRevisions method"
linktitle: "StopTrackRevisions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::StopTrackRevisions method. يوقف العلامة التلقائية لتغييرات المستند كتنقيحات في C++."
type: docs
weight: 93000
url: /ar/cpp/aspose.words/document/stoptrackrevisions/
---
## Document::StopTrackRevisions method


يوقف وضع العلامة التلقائي على تغييرات المستند كمراجعات.

```cpp
void Aspose::Words::Document::StopTrackRevisions()
```


## أمثلة



يظهر كيفية تتبع التنقيحات أثناء تحرير مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// تحرير مستند عادة لا يُحتسب كتنقيح حتى نبدأ في تتبعه.
builder->Write(u"Hello world! ");

ASSERT_EQ(0, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(0)->get_IsInsertRevision());

doc->StartTrackRevisions(u"John Doe");

builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(1)->get_IsInsertRevision());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
ASSERT_TRUE((System::DateTime::get_Now() - doc->get_Revisions()->idx_get(0)->get_DateTime()).get_Milliseconds() <= 10);

// أوقف تتبع التنقيحات لكي لا تُحتسب أي تعديلات مستقبلية كتنقيحات.
doc->StopTrackRevisions();
builder->Write(u"Hello again! ");

ASSERT_EQ(1, doc->get_Revisions()->get_Count());
ASSERT_FALSE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(0)->get_Runs()->idx_get(2)->get_IsInsertRevision());

// إنشاء التنقيحات يمنحها تاريخ ووقت العملية.
// يمكننا تعطيل ذلك بتمرير DateTime.MinValue عندما نبدأ تتبع المراجعات.
doc->StartTrackRevisions(u"John Doe", System::DateTime::MinValue);
builder->Write(u"Hello again! ");

ASSERT_EQ(2, doc->get_Revisions()->get_Count());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(1)->get_Author());
ASSERT_EQ(System::DateTime::MinValue, doc->get_Revisions()->idx_get(1)->get_DateTime());

// يمكننا قبول/رفض هذه المراجعات برمجيًا
// عن طريق استدعاء طرق مثل Document.AcceptAllRevisions، أو طريقة Accept لكل مراجعة.
// في Microsoft Word، يمكننا معالجتها يدويًا عبر "Review" -> "Changes".
doc->Save(get_ArtifactsDir() + u"Revision.StartTrackRevisions.docx");
```

## انظر أيضًا

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
