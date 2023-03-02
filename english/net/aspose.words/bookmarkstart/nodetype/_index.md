---
title: BookmarkStart.NodeType
linktitle: NodeType
second_title: Aspose.Words for .NET API Reference
description: BookmarkStart property. Returns BookmarkStart in C#.
type: docs
weight: 40
url: /net/aspose.words/bookmarkstart/nodetype/
---
## BookmarkStart.NodeType property

Returns BookmarkStart.

```csharp
public override NodeType NodeType { get; }
```

## Examples

Shows how to traverse a composite node's tree of child nodes.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Any node that can contain child nodes, such as the document itself, is composite.
    Assert.True(doc.IsComposite);

    // Invoke the recursive function that will go through and print all the child nodes of a composite node.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Recursively traverses a node tree while printing the type of each node
/// with an indent depending on depth as well as the contents of all inline nodes.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Recurse into the node if it is a composite node. Otherwise, print its contents if it is an inline node.
        if (childNode.IsComposite)
        {
            Console.WriteLine();
            TraverseAllNodes((CompositeNode)childNode, depth + 1);
        }
        else if (childNode is Inline)
        {
            Console.WriteLine($" - \"{childNode.GetText().Trim()}\"");
        }
        else
        {
            Console.WriteLine();
        }
    }
}
```

### See Also

* enum [NodeType](../../nodetype/)
* class [BookmarkStart](../)
* namespace [Aspose.Words](../../bookmarkstart/)
* assembly [Aspose.Words](../../../)
