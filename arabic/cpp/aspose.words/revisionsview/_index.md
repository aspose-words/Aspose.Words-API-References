---
title: "Aspose::Words::RevisionsView enum"
linktitle: "RevisionsView"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::RevisionsView enum. يسمح بتحديد ما إذا كان سيتم العمل بالإصدار الأصلي أو الإصدار المعدل من المستند في C++."
type: docs
weight: 112000
url: /ar/cpp/aspose.words/revisionsview/
---
## RevisionsView enum


يسمح بتحديد ما إذا كان سيتم العمل مع النسخة الأصلية أو النسخة المعدلة من المستند.

```cpp
enum class RevisionsView
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| الأصلي | 0 | يحدد النسخة الأصلية من المستند. |
| النهائي | 1 | يحدد النسخة المعدلة من المستند. |


## أمثلة



يعرض كيفية التبديل بين العرض المعدل والعرض الأصلي للمستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions at list levels.docx");
doc->UpdateListLabels();

System::SharedPtr<Aspose::Words::ParagraphCollection> paragraphs = doc->get_FirstSection()->get_Body()->get_Paragraphs();
ASSERT_EQ(u"1.", paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(System::String::Empty, paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());

// عرض كائن المستند كما لو تم قبول جميع التعديلات. يدعم حاليًا تسميات القوائم.
doc->set_RevisionsView(Aspose::Words::RevisionsView::Final);

ASSERT_EQ(System::String::Empty, paragraphs->idx_get(0)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"1.", paragraphs->idx_get(1)->get_ListLabel()->get_LabelString());
ASSERT_EQ(u"a.", paragraphs->idx_get(2)->get_ListLabel()->get_LabelString());
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
