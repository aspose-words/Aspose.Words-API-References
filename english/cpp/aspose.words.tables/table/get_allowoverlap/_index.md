---
title: Aspose::Words::Tables::Table::get_AllowOverlap method
linktitle: get_AllowOverlap
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Tables::Table::get_AllowOverlap method. Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. Default value is true in C++.'
type: docs
weight: 14000
url: /cpp/aspose.words.tables/table/get_allowoverlap/
---
## Table::get_AllowOverlap method


Gets whether a floating table shall allow other floating objects in the document to overlap its extents when displayed. Default value is **true**.

```cpp
bool Aspose::Words::Tables::Table::get_AllowOverlap()
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

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
