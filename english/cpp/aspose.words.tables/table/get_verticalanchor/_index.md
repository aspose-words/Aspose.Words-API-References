---
title: get_VerticalAnchor
second_title: Aspose.Words for C++ API Reference
description: Gets the base object from which the vertical positioning of floating table should be calculated. Default value is Margin.
type: docs
weight: 508
url: /cpp/aspose.words.tables/table/get_verticalanchor/
---
## Table.get_VerticalAnchor method


Gets the base object from which the vertical positioning of floating table should be calculated. Default value is **Margin**.

```cpp
Aspose::Words::Drawing::RelativeVerticalPosition Aspose::Words::Tables::Table::get_VerticalAnchor()
```


## Examples




Shows how to work with floating tables properties. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Table wrapped by text.docx");

SharedPtr<Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

if (table->get_TextWrapping() == TextWrapping::Around)
{
    ASSERT_EQ(RelativeHorizontalPosition::Margin, table->get_HorizontalAnchor());
    ASSERT_EQ(RelativeVerticalPosition::Paragraph, table->get_VerticalAnchor());
    ASPOSE_ASSERT_EQ(false, table->get_AllowOverlap());

    // Only Margin, Page, Column available in RelativeHorizontalPosition for HorizontalAnchor setter.
    // The ArgumentException will be thrown for any other values.
    table->set_HorizontalAnchor(RelativeHorizontalPosition::Column);

    // Only Margin, Page, Paragraph available in RelativeVerticalPosition for VerticalAnchor setter.
    // The ArgumentException will be thrown for any other values.
    table->set_VerticalAnchor(RelativeVerticalPosition::Page);
}
```

