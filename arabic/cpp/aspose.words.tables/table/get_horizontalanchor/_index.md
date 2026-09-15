---
title: "طريقة Aspose::Words::Tables::Table::get_HorizontalAnchor"
linktitle: "get_HorizontalAnchor"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::Table::get_HorizontalAnchor. يحصل على الكائن الأساسي الذي يجب حساب تموضع الجدول العائم أفقيًا منه. القيمة الافتراضية هي Column في C++."
type: docs
weight: 24000
url: /ar/cpp/aspose.words.tables/table/get_horizontalanchor/
---
## Table::get_HorizontalAnchor method


يحصل على الكائن الأساسي الذي يجب حساب تموضع الجدول العائم أفقيًا منه. القيمة الافتراضية هي [Column](../../../aspose.words.drawing/relativehorizontalposition/).

```cpp
Aspose::Words::Drawing::RelativeHorizontalPosition Aspose::Words::Tables::Table::get_HorizontalAnchor()
```


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

* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
