---
title: CompositeNode.CreateNavigator
linktitle: CreateNavigator
second_title: Aspose.Words for .NET API Reference
description: CompositeNode CreateNavigator method. Creates navigator which can be used to traverse and read nodes in C#.
type: docs
weight: 80
url: /net/aspose.words/compositenode/createnavigator/
---
## CreateNavigator method

Creates navigator which can be used to traverse and read nodes.

```csharp
[EditorBrowsable(EditorBrowsableState.Never)]
public XPathNavigator CreateNavigator()
```

## Examples

Shows how to create an XPathNavigator, and then use it to traverse and read nodes.

```csharp
public void NodeXPathNavigator()
{
    Document doc = new Document();
    XPathNavigator navigator = doc.CreateNavigator();

    if (navigator != null)
    {
        Assert.AreEqual("Document", navigator.Name);
        Assert.AreEqual(false, navigator.MoveToNext());
        Assert.AreEqual(1, navigator.SelectChildren(XPathNodeType.All).Count);

        // The document tree has the document, first section,
        // body, and first paragraph as nodes, with each being an only child of the previous.
        // We can add a few more to give the tree some branches for the navigator to traverse.
        DocumentBuilder docBuilder = new DocumentBuilder(doc);
        docBuilder.Write("Section 1, Paragraph 1. ");
        docBuilder.InsertParagraph();
        docBuilder.Write("Section 1, Paragraph 2. ");
        doc.AppendChild(new Section(doc));
        docBuilder.MoveToSection(1);
        docBuilder.Write("Section 2, Paragraph 1. ");

        // Use our navigator to print a map of all the nodes in the document to the console.
        StringBuilder stringBuilder = new StringBuilder();
        MapDocument(navigator, stringBuilder, 0);
        Console.Write(stringBuilder.ToString());
    }
}

/// <summary>
/// Traverses all children of a composite node and map the structure in the style of a directory tree.
/// The amount of space indentation indicates depth relative to the initial node.
/// Prints the text contents of the current node only if it is a Run.
/// </summary>
private static void MapDocument(XPathNavigator navigator, StringBuilder stringBuilder, int depth)
{
    do
    {
        stringBuilder.Append(' ', depth);
        stringBuilder.Append(navigator.Name + ": ");

        if (navigator.Name == "Run")
        {
            stringBuilder.Append(navigator.Value);
        }

        stringBuilder.Append('\n');

        if (navigator.HasChildren)
        {
            navigator.MoveToFirstChild();
            MapDocument(navigator, stringBuilder, depth + 1);
            navigator.MoveToParent();
        }
    } while (navigator.MoveToNext());
}
```

### See Also

* class [CompositeNode](../)
* namespace [Aspose.Words](../../compositenode/)
* assembly [Aspose.Words](../../../)
