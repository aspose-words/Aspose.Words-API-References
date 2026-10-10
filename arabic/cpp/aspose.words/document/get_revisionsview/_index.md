---
title: "طريقة Aspose::Words::Document::get_RevisionsView"
linktitle: "get_RevisionsView"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Document::get_RevisionsView. يحصل أو يحدد قيمة تشير إلى ما إذا كان سيتم العمل بالإصدار الأصلي أو المعدل من المستند في C++."
type: docs
weight: 47000
url: /ar/cpp/aspose.words/document/get_revisionsview/
---
## Document::get_RevisionsView method


يحصل على أو يضبط قيمة تشير إلى ما إذا كان سيتم العمل بالإصدار الأصلي أو المعدل من المستند.

```cpp
Aspose::Words::RevisionsView Aspose::Words::Document::get_RevisionsView() const
```


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

* Enum [RevisionsView](../../revisionsview/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
