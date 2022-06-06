---
title: GetChildNodes
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 100
url: /net/aspose.words/compositenode/getchildnodes/
---
## CompositeNode.GetChildNodes method

Returns a live collection of child nodes that match the specified type.

```csharp
public NodeCollection GetChildNodes(NodeType nodeType, bool isDeep)
```

| Parameter | Type | Description |
| --- | --- | --- |
| nodeType | NodeType | Specifies the type of nodes to select. |
| isDeep | Boolean | True to select from all child nodes recursively. False to select only among immediate children. |

### Return Value

A live collection of child nodes of the specified type.

## Remarks

The collection of nodes returned by this method is always live.

A live collection is always in sync with the document. For example, if you selected all sections in a document and enumerate through the collection deleting the sections, the section is removed from the collection immediately when it is removed from the document.

## Examples

Shows how to print all of a document's comments and their replies.

```csharp
Document doc = new Document(MyDir + "Comments.docx");

NodeCollection comments = doc.GetChildNodes(NodeType.Comment, true);

// If a comment has no ancestor, it is a "top-level" comment as opposed to a reply-type comment.
// Print all top-level comments along with any replies they may have.
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null))
{
    Console.WriteLine("Top-level comment:");
    Console.WriteLine($"\t\"{comment.GetText().Trim()}\", by {comment.Author}");
    Console.WriteLine($"Has {comment.Replies.Count} replies");
    foreach (Comment commentReply in comment.Replies)
    {
        Console.WriteLine($"\t\"{commentReply.GetText().Trim()}\", by {commentReply.Author}");
    }
    Console.WriteLine();
}
```

Shows how to extract images from a document, and save them to the local file system as individual files.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Get the collection of shapes from the document,
// and save the image data of every shape with an image as a file to the local file system.
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.Count(s => ((Shape)s).HasImage));

int imageIndex = 0;
foreach (Shape shape in shapes.OfType<Shape>())
{
    if (shape.HasImage)
    {
        // The image data of shapes may contain images of many possible image formats. 
        // We can determine a file extension for each image automatically, based on its format.
        string imageFileName =
            $"File.ExtractImages.{imageIndex}{FileFormatUtil.ImageTypeToExtension(shape.ImageData.ImageType)}";
        shape.ImageData.Save(ArtifactsDir + imageFileName);
        imageIndex++;
    }
}
```

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```csharp
Document doc = new Document();

// An empty document, by default, has one paragraph.
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// Composite nodes such as our paragraph can contain other composite and inline nodes as children.
Paragraph paragraph = doc.FirstSection.Body.FirstParagraph;
Run paragraphText = new Run(doc, "Initial text. ");
paragraph.AppendChild(paragraphText);

// Create three more run nodes.
Run run1 = new Run(doc, "Run 1. ");
Run run2 = new Run(doc, "Run 2. ");
Run run3 = new Run(doc, "Run 3. ");

// The document body will not display these runs until we insert them into a composite node
// that itself is a part of the document's node tree, as we did with the first run.
// We can determine where the text contents of nodes that we insert
// appears in the document by specifying an insertion location relative to another node in the paragraph.
Assert.AreEqual("Initial text.", paragraph.GetText().Trim());

// Insert the second run into the paragraph in front of the initial run.
paragraph.InsertBefore(run2, paragraphText);

Assert.AreEqual("Run 2. Initial text.", paragraph.GetText().Trim());

// Insert the third run after the initial run.
paragraph.InsertAfter(run3, paragraphText);

Assert.AreEqual("Run 2. Initial text. Run 3.", paragraph.GetText().Trim());

// Insert the first run to the start of the paragraph's child nodes collection.
paragraph.PrependChild(run1);

Assert.AreEqual("Run 1. Run 2. Initial text. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(4, paragraph.GetChildNodes(NodeType.Any, true).Count);

// We can modify the contents of the run by editing and deleting existing child nodes.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.AreEqual("Run 1. Updated run 2. Run 3.", paragraph.GetText().Trim());
Assert.AreEqual(3, paragraph.GetChildNodes(NodeType.Any, true).Count);
```

### See Also

* class [NodeCollection](../../nodecollection)
* enum [NodeType](../../nodetype)
* class [CompositeNode](../../compositenode)
* namespace [Aspose.Words](../../compositenode)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
