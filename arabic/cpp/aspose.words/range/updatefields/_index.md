---
title: "Aspose::Words::Range::UpdateFields طريقة"
linktitle: "UpdateFields"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Range::UpdateFields. تُحدّث قيم حقول المستند في هذا النطاق في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words/range/updatefields/
---
## Range::UpdateFields method


يحدّث قيم حقول المستند في هذا النطاق.

```cpp
void Aspose::Words::Range::UpdateFields()
```

## ملاحظات


عند فتحك وتعديلك ثم حفظ مستند، لا تقوم Aspose.Words بتحديث الحقول تلقائيًا، بل تحتفظ بها كما هي. لذلك، عادةً ما ترغب في استدعاء هذه الطريقة قبل الحفظ إذا قمت بتعديل المستند برمجيًا وتريد التأكد من ظهور القيم الصحيحة (المُحسوبة) للحقول في المستند المحفوظ.

ليس هناك حاجة لتحديث الحقول بعد تنفيذ دمج البريد لأن دمج البريد هو نوع من تحديث الحقول ويقوم تلقائيًا بتحديث جميع الحقول في المستند.

هذه الطريقة لا تقوم بتحديث جميع أنواع الحقول. للحصول على القائمة التفصيلية لأنواع الحقول المدعومة، راجع دليل المبرمجين.

هذه الطريقة لا تُحدّث الحقول المرتبطة بخوارزميات تخطيط الصفحة (مثل PAGE، PAGES، PAGEREF). يتم تحديث الحقول المتعلقة بتخطيط الصفحة عندما تقوم بعرض مستند أو تستدعي [UpdatePageLayout](../../document/updatepagelayout/).

لتحديث الحقول في المستند بأكمله استخدم [UpdateFields](../../document/updatefields/).

## أمثلة



يظهر كيفية تحديث جميع الحقول في نطاق.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DOCPROPERTY Category");
builder->InsertBreak(Aspose::Words::BreakType::SectionBreakEvenPage);
builder->InsertField(u" DOCPROPERTY Category");

// ستعرض حقول DOCPROPERTY أعلاه قيمة خاصية المستند المدمجة هذه.
doc->get_BuiltInDocumentProperties()->set_Category(u"MyCategory");

// إذا قمنا بتحديث قيمة خاصية المستند، سنحتاج إلى تحديث جميع حقول DOCPROPERTY لعرضها.
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// قم بتحديث جميع الحقول الموجودة في نطاق القسم الأول.
doc->get_FirstSection()->get_Range()->UpdateFields();

ASSERT_EQ(u"MyCategory", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(System::String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
```

## انظر أيضًا

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
