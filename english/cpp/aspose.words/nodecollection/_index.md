---
title: NodeCollection
second_title: Aspose.Words for C++ API Reference
description: Represents a collection of nodes of a specific type.
type: docs
weight: 547
url: /cpp/aspose.words/nodecollection/
---
## NodeCollection class


Represents a collection of nodes of a specific type.

```cpp
class NodeCollection : public Aspose::Words::INodeCollection,
                       public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Node>>
```

## Methods

| Method | Description |
| --- | --- |
| [Add](./add/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Adds a node to the end of the collection. |
| [Clear](./clear/)() | Removes all nodes from this collection and from the document. |
| [Contains](./contains/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Determines whether a node is in the collection. |
| [get_Count](./get_count/)() | Gets the number of nodes in the collection. |
| [GetEnumerator](./getenumerator/)() override | Provides a simple "foreach" style iteration over the collection of nodes. |
| [idx_get](./idx_get/)(int32_t) | Retrieves a node at the given index. |
| [IndexOf](./indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the zero-based index of the specified node. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts a node into the collection at the specified index. |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the node from the collection and from the document. |
| [RemoveAt](./removeat/)(int32_t) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](./toarray/)() | Copies all nodes from the collection to a new array of nodes. |
## Remarks


**NodeCollection** does not own the nodes it contains, rather, is just a selection of nodes of the specified type, but the nodes are stored in the tree under their respective parent nodes.

**NodeCollection** supports indexed access, iteration and provides add and remove methods.

The **NodeCollection** collection is "live", i.e. changes to the children of the node object that it was created from are immediately reflected in the nodes returned by the **NodeCollection** properties and methods.

**NodeCollection** is returned by [GetChildNodes()](../compositenode/getchildnodes/) and also serves as a base class for typed node collections such as [SectionCollection](../sectioncollection/), [ParagraphCollection](../paragraphcollection/) etc.

**NodeCollection** can be "flat" and contain only immediate children of the node it was created from, or it can be "deep" and contain all descendant children.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
