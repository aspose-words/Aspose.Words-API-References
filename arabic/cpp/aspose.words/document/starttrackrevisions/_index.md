---
title: "Aspose::Words::Document::StartTrackRevisions method"
linktitle: "StartTrackRevisions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::StartTrackRevisions. يبدأ تلقائيًا بوضع علامة على جميع التغييرات اللاحقة التي تقوم بها على المستند برمجيًا كالتغييرات المراجعية في C++."
type: docs
weight: 92000
url: /ar/cpp/aspose.words/document/starttrackrevisions/
---
## Document::StartTrackRevisions(const System::String\&) method


يبدأ تلقائيًا بوضع علامة على جميع التغييرات اللاحقة التي تُجريها على المستند برمجيًا كالتغييرات المراجعية.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| المؤلف | const System::String\& | الأحرف الأولى للمؤلف لاستخدامها في المراجعات. |
## ملاحظات


إذا قمت باستدعاء هذه الطريقة ثم أجريت بعض التغييرات على المستند برمجياً، احفظ المستند ولاحقاً افتحه في MS Word سترى هذه التغييرات كتنقيحات.

حاليًا يدعم Aspose.Words تتبع إدراجات العقد وحذفها فقط. لا يتم تسجيل تغييرات التنسيق كتنقيحات.

يتم دعم التتبع التلقائي للتغييرات سواء عند تعديل هذا المستند عبر عمليات معالجة العقد أو عند استخدام [DocumentBuilder](../../documentbuilder/)

هذه الطريقة لا تغير خيار [TrackRevisions](../get_trackrevisions/) ولا تستخدم قيمته لأغراض تتبع التنقيحات.

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
## Document::StartTrackRevisions(const System::String\&, System::DateTime) method


يبدأ تلقائيًا بوضع علامة على جميع التغييرات اللاحقة التي تُجريها على المستند برمجيًا كالتغييرات المراجعية.

```cpp
void Aspose::Words::Document::StartTrackRevisions(const System::String &author, System::DateTime dateTime)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| المؤلف | const System::String\& | الأحرف الأولى للمؤلف لاستخدامها في المراجعات. |
| dateTime | System::DateTime | التاريخ والوقت لاستخدامهما في المراجعات. |
## ملاحظات


إذا قمت باستدعاء هذه الطريقة ثم أجريت بعض التغييرات على المستند برمجياً، احفظ المستند ولاحقاً افتحه في MS Word سترى هذه التغييرات كتنقيحات.

حاليًا يدعم Aspose.Words تتبع إدراجات العقد وحذفها فقط. لا يتم تسجيل تغييرات التنسيق كتنقيحات.

يتم دعم التتبع التلقائي للتغييرات سواء عند تعديل هذا المستند عبر عمليات معالجة العقد أو عند استخدام [DocumentBuilder](../../documentbuilder/)

هذه الطريقة لا تغير خيار [TrackRevisions](../get_trackrevisions/) ولا تستخدم قيمته لأغراض تتبع التنقيحات.

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
