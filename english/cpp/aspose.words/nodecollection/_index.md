---
title: Aspose::Words::NodeCollection class
linktitle: NodeCollection
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::NodeCollection class. Represents a collection of nodes of a specific type. To learn more, visit the  documentation article in C++.'
type: docs
weight: 43000
url: /cpp/aspose.words/nodecollection/
---
## NodeCollection class


Represents a collection of nodes of a specific type. To learn more, visit the [Aspose.Words Document Object Model (DOM)](https://docs.aspose.com/words/cpp/aspose-words-document-object-model/) documentation article.

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
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Retrieves a node at the given index. |
| [IndexOf](./indexof/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Returns the zero-based index of the specified node. |
| [Insert](./insert/)(int32_t, const System::SharedPtr\<Aspose::Words::Node\>\&) | Inserts a node into the collection at the specified index. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Node\>\&) | Removes the node from the collection and from the document. |
| [RemoveAt](./removeat/)(int32_t) | Removes the node at the specified index from the collection and from the document. |
| [ToArray](./toarray/)() | Copies all nodes from the collection to a new array of nodes. |
| static [Type](./type/)() |  |
## Remarks


[NodeCollection](./) does not own the nodes it contains, rather, is just a selection of nodes of the specified type, but the nodes are stored in the tree under their respective parent nodes.

[NodeCollection](./) supports indexed access, iteration and provides add and remove methods.

The [NodeCollection](./) collection is "live", i.e. changes to the children of the node object that it was created from are immediately reflected in the nodes returned by the [NodeCollection](./) properties and methods.

[NodeCollection](./) is returned by [GetChildNodes()](../compositenode/getchildnodes/) and also serves as a base class for typed node collections such as [SectionCollection](../sectioncollection/), [ParagraphCollection](../paragraphcollection/) etc.

[NodeCollection](./) can be "flat" and contain only immediate children of the node it was created from, or it can be "deep" and contain all descendant children.

## Examples



Shows how to replace all textbox shapes with image shapes. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Textboxes in drawing canvas.docx");

System::ArrayPtr<System::SharedPtr<Aspose::Words::Drawing::Shape>> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(3, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::TextBox;
}))));
ASSERT_EQ(1, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::Image;
}))));

for (System::SharedPtr<Aspose::Words::Drawing::Shape> shape : shapes)
{
    if (shape->get_ShapeType() == Aspose::Words::Drawing::ShapeType::TextBox)
    {
        auto replacementShape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
        replacementShape->get_ImageData()->SetImage(get_ImageDir() + u"Logo.jpg");
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

        shape->get_ParentNode()->InsertAfter<System::SharedPtr<Aspose::Words::Drawing::Shape>>(replacementShape, shape);
        shape->Remove();
    }
}

shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()->LINQ_ToArray();

ASSERT_EQ(0, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::TextBox;
}))));
ASSERT_EQ(4, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Drawing::Shape>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Drawing::Shape> s)>>([](System::SharedPtr<Aspose::Words::Drawing::Shape> s) -> bool
{
    return s->get_ShapeType() == Aspose::Words::Drawing::ShapeType::Image;
}))));

doc->Save(get_ArtifactsDir() + u"Shape.ReplaceTextboxesWithImages.docx");
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
