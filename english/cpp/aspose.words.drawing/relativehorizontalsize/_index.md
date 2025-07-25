---
title: Aspose::Words::Drawing::RelativeHorizontalSize enum
linktitle: RelativeHorizontalSize
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::RelativeHorizontalSize enum. Specifies relatively to what the width of a shape or a text frame is calculated horizontally in C++.'
type: docs
weight: 33500
url: /cpp/aspose.words.drawing/relativehorizontalsize/
---
## RelativeHorizontalSize enum


Specifies relatively to what the width of a shape or a text frame is calculated horizontally.

```cpp
enum class RelativeHorizontalSize
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Margin | 0 | Specifies that the width is calculated relatively to the space between the left and the right margins. |
| Page | 1 | Specifies that the width is calculated relatively to the page width. |
| LeftMargin | 2 | Specifies that the width is calculated relatively to the left margin area size. |
| RightMargin | 3 | Specifies that the width is calculated relatively to the right margin area size. |
| InnerMargin | 4 | Specifies that the width is calculated relatively to the inside margin area size, to the left margin area size for odd pages and to the right margin area size for even pages. |
| OuterMargin | 5 | Specifies that the width is calculated relatively to the outside margin area size, to the right margin area size for odd pages and to the left margin area size for even pages. |
| Default | n/a | Default value is [Margin](./). |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
