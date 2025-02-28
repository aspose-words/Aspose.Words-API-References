---
title: Node.NextSibling
linktitle: NextSibling
articleTitle: NextSibling
second_title: Aspose.Words for .NET
description: Discover the Node NextSibling property to easily access the next node in your DOM. Enhance your JavaScript skills and streamline your coding today!
type: docs
weight: 40
url: /net/aspose.words/node/nextsibling/
---
## Node.NextSibling property

Gets the node immediately following this node.

```csharp
public Node NextSibling { get; }
```

## Remarks

If there is no next node, a `null` is returned.

## Examples

Shows how to use a node's NextSibling property to enumerate through its immediate children.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

for (Node node = doc.FirstSection.Body.FirstChild; node != null; node = node.NextSibling)
{
    Console.WriteLine();
    Console.WriteLine($"Node type: {Node.NodeTypeToString(node.NodeType)}");

    string contents = node.GetText().Trim();
    Console.WriteLine(contents == string.Empty ? "This node contains no text" : $"Contents: \"{node.GetText().Trim()}\"");
}
```

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

* class [Node](../)
* namespace [Aspose.Words](../../../aspose.words/)
* assembly [Aspose.Words](../../../)
