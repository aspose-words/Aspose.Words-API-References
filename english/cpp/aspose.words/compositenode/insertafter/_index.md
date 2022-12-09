---
title: InsertAfter
second_title: Aspose.Words for C++ API Reference
description: Inserts the specified node immediately after the specified reference node.
type: docs
weight: 183
url: /cpp/aspose.words/compositenode/insertafter/
---
## CompositeNode::InsertAfter method


Inserts the specified node immediately after the specified reference node.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::CompositeNode::InsertAfter(const System::SharedPtr<Aspose::Words::Node> &newChild, const System::SharedPtr<Aspose::Words::Node> &refChild)
```


| Parameter | Type | Description |
| --- | --- | --- |
| newChild | const System::SharedPtr\<Aspose::Words::Node\>\& | The [Node](../../node/) to insert. |
| refChild | const System::SharedPtr\<Aspose::Words::Node\>\& | The [Node](../../node/) that is the reference node. The *newChild* is placed after the *refChild*. |

### ReturnValue

The inserted node.
## Remarks


If *refChild* is **null**, inserts *newChild* at the beginning of the list of child nodes.

If the *newChild* is already in the tree, it is first removed.

If the node being inserted was created from another document, you should use [ImportNode()](../) to import the node to the current document. The imported node can then be inserted into the current document.

## Examples



Shows how to add, update and delete child nodes in a [CompositeNode](../)'s collection of children. 
```cpp
auto doc = MakeObject<Document>();

// An empty document, by default, has one paragraph.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->get_Paragraphs()->get_Count());

// Composite nodes such as our paragraph can contain other composite and inline nodes as children.
SharedPtr<Paragraph> paragraph = doc->get_FirstSection()->get_Body()->get_FirstParagraph();
auto paragraphText = MakeObject<Run>(doc, u"Initial text. ");
paragraph->AppendChild(paragraphText);

// Create three more run nodes.
auto run1 = MakeObject<Run>(doc, u"Run 1. ");
auto run2 = MakeObject<Run>(doc, u"Run 2. ");
auto run3 = MakeObject<Run>(doc, u"Run 3. ");

// The document body will not display these runs until we insert them into a composite node
// that itself is a part of the document's node tree, as we did with the first run.
// We can determine where the text contents of nodes that we insert
// appears in the document by specifying an insertion location relative to another node in the paragraph.
ASSERT_EQ(u"Initial text.", paragraph->GetText().Trim());

// Insert the second run into the paragraph in front of the initial run.
paragraph->InsertBefore(run2, paragraphText);

ASSERT_EQ(u"Run 2. Initial text.", paragraph->GetText().Trim());

// Insert the third run after the initial run.
paragraph->InsertAfter(run3, paragraphText);

ASSERT_EQ(u"Run 2. Initial text. Run 3.", paragraph->GetText().Trim());

// Insert the first run to the start of the paragraph's child nodes collection.
paragraph->PrependChild(run1);

ASSERT_EQ(u"Run 1. Run 2. Initial text. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(4, paragraph->GetChildNodes(NodeType::Any, true)->get_Count());

// We can modify the contents of the run by editing and deleting existing child nodes.
(System::DynamicCast<Run>(paragraph->GetChildNodes(NodeType::Run, true)->idx_get(1)))->set_Text(u"Updated run 2. ");
paragraph->GetChildNodes(NodeType::Run, true)->Remove(paragraphText);

ASSERT_EQ(u"Run 1. Updated run 2. Run 3.", paragraph->GetText().Trim());
ASSERT_EQ(3, paragraph->GetChildNodes(NodeType::Any, true)->get_Count());
```


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
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
