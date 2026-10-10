---
title: "Aspose::Words::Tables::Table::get_AllowOverlap طريقة"
linktitle: "get_AllowOverlap"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::get_AllowOverlap طريقة. يحصل على ما إذا كان الجدول العائم سيسمح لكائنات عائمة أخرى في المستند بتجاوز حدوده عند العرض. القيمة الافتراضية هي true في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.tables/table/get_allowoverlap/
---
## Table::get_AllowOverlap method


يحصل ما إذا كان الجدول العائم سيسمح لكائنات عائمة أخرى في المستند بتغطية نطاقه عند العرض. القيمة الافتراضية هي **true**.

```cpp
bool Aspose::Words::Tables::Table::get_AllowOverlap()
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

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
