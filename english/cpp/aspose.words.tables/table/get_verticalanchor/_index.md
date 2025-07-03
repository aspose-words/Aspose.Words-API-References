---
title: Aspose::Words::Tables::Table::get_VerticalAnchor method
linktitle: get_VerticalAnchor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_VerticalAnchor method. Gets the base object from which the vertical positioning of floating table should be calculated. Default value is Margin in C++.'
type: docs
weight: 41000
url: /cpp/aspose.words.tables/table/get_verticalanchor/
---
## Table::get_VerticalAnchor method


Gets the base object from which the vertical positioning of floating table should be calculated. Default value is [Margin](../../../aspose.words.drawing/relativeverticalposition/).

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Tables::Table::get_VerticalAnchor()
```


## Examples



Shows how to work with floating tables properties. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == Aspose::Words::Tables::TextWrapping::Around)
{
    ASSERT_EQ(Aspose::Words::Drawing::RelativeHorizontalPosition::Margin, table->get_HorizontalAnchor());
    ASSERT_EQ(Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph, table->get_VerticalAnchor());
    ASPOSE_ASSERT_EQ(false, table->get_AllowOverlap());

    // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
    // The ArgumentException will be thrown for any other values.
    table->set_HorizontalAnchor(Aspose::Words::Drawing::RelativeHorizontalPosition::Column);

    // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
    // The ArgumentException will be thrown for any other values.
    table->set_VerticalAnchor(Aspose::Words::Drawing::RelativeVerticalPosition::Page);
}
```

## See Also

* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
