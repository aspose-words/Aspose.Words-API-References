---
title: "طريقة Aspose::Words::Range::Delete"
linktitle: "حذف"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Range::Delete. تحذف جميع الأحرف في النطاق في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/range/delete/
---
## Range::Delete method


يحذف جميع الأحرف في النطاق.

```cpp
void Aspose::Words::Range::Delete()
```


## أمثلة



يظهر كيفية حذف جميع العقد من نطاق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف نصًا إلى القسم الأول في المستند، ثم أضف قسمًا آخر.
builder->Write(u"Section 1. ");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakContinuous);
builder->Write(u"Section 2.");

ASSERT_EQ(u"Section 1. \fSection 2.", doc->GetText().Trim());

// قم بإزالة القسم الأول بالكامل عن طريق حذف جميع العقد
// داخل نطاقه، بما في ذلك القسم نفسه.
doc->get_Sections()->idx_get(0)->get_Range()->Delete();

ASSERT_EQ(1, doc->get_Sections()->get_Count());
ASSERT_EQ(u"Section 2.", doc->GetText().Trim());
```

## انظر أيضًا

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
