---
title: Aspose::Words::Drawing::WrapSide enum
linktitle: WrapSide
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::WrapSide enum. Specifies what side(s) of the shape or picture the text wraps around in C++.'
type: docs
weight: 44000
url: /cpp/aspose.words.drawing/wrapside/
---
## WrapSide enum


Specifies what side(s) of the shape or picture the text wraps around.

```cpp
enum class WrapSide
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Both | 0 | The document text wraps on both sides of the shape. |
| Left | 1 | The document text wraps on the left side of the shape only. There is a text free area on the right of the shape. |
| Right | 2 | The document text wraps on the right side of the shape only. There is a text free area on the left side of the shape. |
| Largest | 3 | The document text wraps on the side of the shape that is farthest from the page margin, leaving text free area on the other side of the shape. |
| Default | n/a | Default value is [Both](./). |


## Examples



Shows how to replace all textbox shapes with image shapes. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Textboxes in drawing canvas.docx");

ArrayPtr<SharedPtr<Shape>> shapes = doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<SharedPtr<Shape>>()->LINQ_ToArray();

auto isTextBox = [](SharedPtr<Shape> s)
{
    return s->get_ShapeType() == ShapeType::TextBox;
};
auto isImage = [](SharedPtr<Shape> s)
{
    return s->get_ShapeType() == ShapeType::Image;
};
ASSERT_EQ(3, shapes->LINQ_Count(isTextBox));
ASSERT_EQ(1, shapes->LINQ_Count(isImage));

for (SharedPtr<Shape> shape : shapes)
{
    if (shape->get_ShapeType() == ShapeType::TextBox)
    {
        auto replacementShape = MakeObject<Shape>(doc, ShapeType::Image);
        replacementShape->get_ImageData()->SetImage(ImageDir + u"Logo.jpg");
        replacementShape->set_Left(shape->get_Left());
        replacementShape->set_Top(shape->get_Top());
        replacementShape->set_Width(shape->get_Width());
        replacementShape->set_Height(shape->get_Height());
        replacementShape->set_RelativeHorizontalPosition(shape->get_RelativeHorizontalPosition());
        replacementShape->set_RelativeVerticalPosition(shape->get_RelativeVerticalPosition());
        replacementShape->set_HorizontalAlignment(shape->get_HorizontalAlignment());
        replacementShape->set_VerticalAlignment(shape->get_VerticalAlignment());
        replacementShape->set_WrapType(shape->get_WrapType());
        replacementShape->set_WrapSide(shape->get_WrapSide());

        shape->get_ParentNode()->InsertAfter(replacementShape, shape);
        shape->Remove();
    }
}

shapes = doc->GetChildNodes(NodeType::Shape, true)->LINQ_OfType<SharedPtr<Shape>>()->LINQ_ToArray();

ASSERT_EQ(0, shapes->LINQ_Count(isTextBox));
ASSERT_EQ(4, shapes->LINQ_Count(isImage));

doc->Save(ArtifactsDir + u"Shape.ReplaceTextboxesWithImages.docx");
```

## See Also

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
