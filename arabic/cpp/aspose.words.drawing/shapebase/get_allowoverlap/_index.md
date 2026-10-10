---
title: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap طريقة"
linktitle: "get_AllowOverlap"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::ShapeBase::get_AllowOverlap طريقة. يحصل على أو يحدد قيمة تحدد ما إذا كان هذا الشكل يمكن أن يتداخل مع أشكال أخرى في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.drawing/shapebase/get_allowoverlap/
---
## ShapeBase::get_AllowOverlap method


يحصل أو يضبط قيمة تحدد ما إذا كان هذا الشكل يمكنه التداخل مع أشكال أخرى.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AllowOverlap()
```

## ملاحظات


هذه الخاصية تؤثر على سلوك الشكل في Microsoft Word. Aspose.Words يتجاهل قيمة هذه الخاصية.

هذه الخاصية تنطبق فقط على الأشكال ذات المستوى الأعلى.

القيمة الافتراضية هي **true**.

## أمثلة



يوضح كيفية العمل مع خصائص الجداول العائمة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == Aspose::Words::Tables::TextWrapping::Around)
{
    ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, table->get_HorizontalAnchor());
    ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, table->get_VerticalAnchor());
    ASPOSE_ASSERT_EQ(false, table->get_AllowOverlap());

    // فقط Margin و Page و Column متاحة في RelativeHorizontalPosition لمُعيّن HorizontalAnchor.
    // سيتم إلقاء استثناء ArgumentException لأي قيم أخرى.
    table->set_HorizontalAnchor(Aspose::Words::Drawing::RelativeHorizontalPosition::Column);

    // فقط Margin و Page و Paragraph متاحة في RelativeVerticalPosition لمُعيّن VerticalAnchor.
    // سيتم إلقاء استثناء ArgumentException لأي قيم أخرى.
    table->set_VerticalAnchor(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
}
```

## انظر أيضًا

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
