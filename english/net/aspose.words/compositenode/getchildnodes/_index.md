---
title: CompositeNode.GetChildNodes
linktitle: GetChildNodes
articleTitle: GetChildNodes
second_title: Aspose.Words for .NET
description: Discover the CompositeNode GetChildNodes method—effortlessly retrieve a live collection of child nodes tailored to your specified type for enhanced performance.
type: docs
weight: 110
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
| isDeep | Boolean | `true` to select from all child nodes recursively; `false` to select only among immediate children. |

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
foreach (Comment comment in comments.OfType<Comment>().Where(c => c.Ancestor == null).ToList())
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

Assert.That(shapes.Count(s => ((Shape)s).HasImage), Is.EqualTo(9));

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

Shows how to traverse through a composite node's collection of child nodes.

```csharp
Document doc = new Document();

// Add two runs and one shape as child nodes to the first paragraph of this document.
Paragraph paragraph = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
paragraph.AppendChild(new Run(doc, "Hello world! "));

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
// Note that the 'CustomNodeId' is not saved to an output file and exists only during the node lifetime.
shape.CustomNodeId = 100;
shape.WrapType = WrapType.Inline;
paragraph.AppendChild(shape);

paragraph.AppendChild(new Run(doc, "Hello again!"));

// Iterate through the paragraph's collection of immediate children,
// and print any runs or shapes that we find within.
NodeCollection children = paragraph.GetChildNodes(NodeType.Any, false);

Assert.That(paragraph.GetChildNodes(NodeType.Any, false).Count, Is.EqualTo(3));

foreach (Node child in children)
    switch (child.NodeType)
    {
        case NodeType.Run:
            Console.WriteLine("Run contents:");
            Console.WriteLine($"\t\"{child.GetText().Trim()}\"");
            break;
        case NodeType.Shape:
            Shape childShape = (Shape)child;
            Console.WriteLine("Shape:");
            Console.WriteLine($"\t{childShape.ShapeType}, {childShape.Width}x{childShape.Height}");
            break;
    }
```

Shows how to add, update and delete child nodes in a CompositeNode's collection of children.

```csharp
Document doc = new Document();

// An empty document, by default, has one paragraph.
Assert.That(doc.FirstSection.Body.Paragraphs.Count, Is.EqualTo(1));

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
Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Initial text."));

// Insert the second run into the paragraph in front of the initial run.
paragraph.InsertBefore(run2, paragraphText);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 2. Initial text."));

// Insert the third run after the initial run.
paragraph.InsertAfter(run3, paragraphText);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 2. Initial text. Run 3."));

// Insert the first run to the start of the paragraph's child nodes collection.
paragraph.PrependChild(run1);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 1. Run 2. Initial text. Run 3."));
Assert.That(paragraph.GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(4));

// We can modify the contents of the run by editing and deleting existing child nodes.
((Run)paragraph.GetChildNodes(NodeType.Run, true)[1]).Text = "Updated run 2. ";
paragraph.GetChildNodes(NodeType.Run, true).Remove(paragraphText);

Assert.That(paragraph.GetText().Trim(), Is.EqualTo("Run 1. Updated run 2. Run 3."));
Assert.That(paragraph.GetChildNodes(NodeType.Any, true).Count, Is.EqualTo(3));
```

### See Also

* class [NodeCollection](../../nodecollection/)
* enum [NodeType](../../nodetype/)
* class [CompositeNode](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
