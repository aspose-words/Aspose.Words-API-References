---
title: Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize method
linktitle: get_RelativeHorizontalSize
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize method. Gets or sets the value of shape''s relative size in horizontal direction in C++.'
type: docs
weight: 42500
url: /cpp/aspose.words.drawing/shapebase/get_relativehorizontalsize/
---
## ShapeBase::get_RelativeHorizontalSize method


Gets or sets the value of shape's relative size in horizontal direction.

```cpp
Aspose::Words::Drawing::RelativeHorizontalSize Aspose::Words::Drawing::ShapeBase::get_RelativeHorizontalSize()
```

## Remarks


The default value is [RelativeHorizontalSize](../../relativehorizontalsize/).

Has effect only if [WidthRelative](../get_widthrelative/) is set.

## Examples



Shows how to set relative size and position. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Adding a simple shape with absolute size and position.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 40);
// Set WrapType to WrapType.None since Inline shapes are automatically converted to absolute units.
shape->set_WrapType(Aspose::Words::Drawing::WrapType::None);

// Checking and setting the relative horizontal size.
if (shape->get_RelativeHorizontalSize() == Aspose::Words::Drawing::RelativeHorizontalSize::Default)
{
    // Setting the horizontal size binding to Margin.
    shape->set_RelativeHorizontalSize(Aspose::Words::Drawing::RelativeHorizontalSize::Margin);
    // Setting the width to 50% of Margin width.
    shape->set_WidthRelative(50.0f);
}

// Checking and setting the relative vertical size.
if (shape->get_RelativeVerticalSize() == Aspose::Words::Drawing::RelativeVerticalSize::Default)
{
    // Setting the vertical size binding to Margin.
    shape->set_RelativeVerticalSize(Aspose::Words::Drawing::RelativeVerticalSize::Margin);
    // Setting the heigh to 30% of Margin height.
    shape->set_HeightRelative(30.0f);
}

// Checking and setting the relative vertical position.
if (shape->get_RelativeVerticalPosition() == Aspose::Words::Drawing::RelativeVerticalPosition::Paragraph)
{
    // etting the position binding to TopMargin.
    shape->set_RelativeVerticalPosition(Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin);
    // Setting relative Top to 30% of TopMargin position.
    shape->set_TopRelative(30.0f);
}

// Checking and setting the relative horizontal position.
if (shape->get_RelativeHorizontalPosition() == Aspose::Words::Drawing::RelativeHorizontalPosition::Default)
{
    // Setting the position binding to RightMargin.
    shape->set_RelativeHorizontalPosition(Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin);
    // The position relative value can be negative.
    shape->set_LeftRelative(-260.0f);
}

doc->Save(get_ArtifactsDir() + u"Shape.RelativeSizeAndPosition.docx");
```

## See Also

* Enum [RelativeHorizontalSize](../../relativehorizontalsize/)
* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
