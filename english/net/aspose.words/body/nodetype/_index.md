---
title: Body.NodeType
linktitle: NodeType
second_title: Aspose.Words for .NET API Reference
description: Body property. Returns Body in C#.
type: docs
weight: 20
url: /net/aspose.words/body/nodetype/
---
## Body.NodeType property

Returns Body.

```csharp
public override NodeType NodeType { get; }
```

## Examples

Shows how to iterate through the children of a composite node.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// A Section is a composite node and can contain child nodes,
// but only if those child nodes are of a "Body" or "HeaderFooter" node type.
foreach (Node node in section)
{
    switch (node.NodeType)
    {
        case NodeType.Body:
        {
            Body body = (Body)node;

            Console.WriteLine("Body:");
            Console.WriteLine($"\t\"{body.GetText().Trim()}\"");
            break;
        }
        case NodeType.HeaderFooter:
        {
            HeaderFooter headerFooter = (HeaderFooter)node;

            Console.WriteLine($"HeaderFooter type: {headerFooter.HeaderFooterType}:");
            Console.WriteLine($"\t\"{headerFooter.GetText().Trim()}\"");
            break;
        }
        default:
        {
            throw new Exception("Unexpected node type in a section.");
        }
    }
}
```

### See Also

* enum [NodeType](../../nodetype/)
* class [Body](../)
* namespace [Aspose.Words](../../body/)
* assembly [Aspose.Words](../../../)
