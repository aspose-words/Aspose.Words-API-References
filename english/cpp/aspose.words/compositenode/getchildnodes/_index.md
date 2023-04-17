---
title: Aspose::Words::CompositeNode::GetChildNodes method
linktitle: GetChildNodes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::CompositeNode::GetChildNodes method. Returns a live collection of child nodes that match the specified type in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words/compositenode/getchildnodes/
---
## CompositeNode::GetChildNodes method


Returns a live collection of child nodes that match the specified type.

```cpp
System::SharedPtr<Aspose::Words::NodeCollection> Aspose::Words::CompositeNode::GetChildNodes(Aspose::Words::NodeType nodeType, bool isDeep)
```


| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | Aspose::Words::NodeType | Specifies the type of nodes to select. |
| isDeep | bool | **true** to select from all child nodes recursively; **false** to select only among immediate children. |

### ReturnValue

A live collection of child nodes of the specified type.
## Remarks


The collection of nodes returned by this method is always live.

A live collection is always in sync with the document. For example, if you selected all sections in a document and enumerate through the collection deleting the sections, the section is removed from the collection immediately when it is removed from the document.

## Examples



Shows how to print all of a document's comments and their replies. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Comments.docx");

SharedPtr<NodeCollection> comments = doc->GetChildNodes(NodeType::Comment, true);

// If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
// Print all top-level comments along with any replies they may have.
auto hasNullAncestor = [](SharedPtr<Comment> c)
{
    return c->get_Ancestor() == nullptr;
};

for (auto comment : System::IterateOver(comments->LINQ_OfType<SharedPtr<Comment>>()->LINQ_Where(hasNullAncestor)))
{
    std::cout << "Top-level comment:" << std::endl;
    std::cout << "\t\"" << comment->GetText().Trim() << "\", by " << comment->get_Author() << std::endl;
    std::cout << "Has " << comment->get_Replies()->get_Count() << " replies" << std::endl;
    for (const auto& commentReply : System::IterateOver<Comment>(comment->get_Replies()))
    {
        std::cout << "\t\"" << commentReply->GetText().Trim() << "\", by " << commentReply->get_Author() << std::endl;
    }
    std::cout << std::endl;
}
```


Shows how to extract images from a document, and save them to the local file system as individual files. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
SharedPtr<NodeCollection> shapes = doc->GetChildNodes(NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count([](SharedPtr<Node> s) { return (System::DynamicCast<Shape>(s))->get_HasImage(); }));

int imageIndex = 0;
for (const auto& shape : System::IterateOver(shapes->LINQ_OfType<SharedPtr<Shape>>()))
{
    if (shape->get_HasImage())
    {
        // The image data of shapes may contain images of many possible image formats.
        // We can determine a file extension for each image automatically, based on its format.
        String imageFileName =
            String::Format(u"File.ExtractImages.{0}{1}", imageIndex, FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```


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

## See Also

* Class [NodeCollection](../../nodecollection/)
* Enum [NodeType](../../nodetype/)
* Class [CompositeNode](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
