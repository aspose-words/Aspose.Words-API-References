---
title: get_HorizontalAnchor
second_title: Aspose.Words for C++ API Reference
description: Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is Column.
type: docs
weight: 300
url: /cpp/aspose.words.tables/table/get_horizontalanchor/
---
## Table::get_HorizontalAnchor method


Gets the base object from which the horizontal positioning of floating table should be calculated. Default value is [Column](../../../aspose.words.drawing/relativehorizontalposition/).

```cpp
Aspose::Words::Drawing::RelativeHorizontalPosition Aspose::Words::Tables::Table::get_HorizontalAnchor()
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

## See Also

* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words](../../../)
