---
title: get_AllowOverlap
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value that specifies whether this shape can overlap other shapes.
type: docs
weight: 14
url: /cpp/aspose.words.drawing/shapebase/get_allowoverlap/
---
## ShapeBase.get_AllowOverlap method


Gets or sets a value that specifies whether this shape can overlap other shapes.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_AllowOverlap()
```


This property affects behavior of the shape in Microsoft Word. Aspose.Words ignores the value of this property.

This property is applicable only to top level shapes.

The default value is **true**.

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

