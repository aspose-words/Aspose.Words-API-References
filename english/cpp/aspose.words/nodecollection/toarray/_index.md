---
title: ToArray
second_title: Aspose.Words for C++ API Reference
description: Copies all nodes from the collection to a new array of nodes.
type: docs
weight: 170
url: /cpp/aspose.words/nodecollection/toarray/
---
## NodeCollection::ToArray method


Copies all nodes from the collection to a new array of nodes.

```cpp
System::ArrayPtr<System::SharedPtr<Aspose::Words::Node>> Aspose::Words::NodeCollection::ToArray()
```


### ReturnValue

An array of nodes.
## Remarks


You should not be adding/removing nodes while iterating over a collection of nodes because it invalidates the iterator and requires refreshes for live collections.

To be able to add/remove nodes during iteration, use this method to copy nodes into a fixed-size array and then iterate over the array.

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

* Class [Node](../../node/)
* Class [NodeCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
