---
title: Aspose::Words::Tables::Table::set_VerticalAnchor method
linktitle: set_VerticalAnchor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::set_VerticalAnchor method. Gets the base object from which the vertical positioning of floating table should be calculated. Default value is Margin in C++.'
type: docs
weight: 132000
url: /cpp/aspose.words.tables/table/set_verticalanchor/
---
## Table::set_VerticalAnchor method


Gets the base object from which the vertical positioning of floating table should be calculated. Default value is [Margin](../../../aspose.words.drawing/relativeverticalposition/).

```cpp
void Aspose::Words::Tables::Table::set_VerticalAnchor(Aspose::Words::Drawing::RelativeVerticalPosition value)
```

## Examples


Shows how to work with floating tables properties.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Table wrapped by text.docx"));

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == TextWrapping::Around)
{
    ASSERT_EQ(table->get_HorizontalAnchor(), RelativeHorizontalPosition::Margin);
    ASSERT_EQ(table->get_VerticalAnchor(), RelativeVerticalPosition::Paragraph);
    ASPOSE_ASSERT_EQ(table->get_AllowOverlap(), false);

    // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
    // The ArgumentException will be thrown for any other values.
    table->set_HorizontalAnchor(RelativeHorizontalPosition::Column);

    // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
    // The ArgumentException will be thrown for any other values.
    table->set_VerticalAnchor(RelativeVerticalPosition::Page);
}
```
## See Also

* [get_VerticalAnchor](../get_verticalanchor/)

* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
