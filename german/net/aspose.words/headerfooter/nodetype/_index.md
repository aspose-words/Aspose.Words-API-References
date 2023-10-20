---
title: HeaderFooter.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words für .NET
description: HeaderFooter NodeType eigendom. Gibt zurückHeaderFooter  in C#.
type: docs
weight: 50
url: /de/net/aspose.words/headerfooter/nodetype/
---
## HeaderFooter.NodeType property

Gibt zurückHeaderFooter .

```csharp
public override NodeType NodeType { get; }
```

## Beispiele

Zeigt, wie die untergeordneten Elemente eines zusammengesetzten Knotens durchlaufen werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// Ein Abschnitt ist ein zusammengesetzter Knoten und kann untergeordnete Knoten enthalten.
// aber nur, wenn diese untergeordneten Knoten vom Knotentyp „Body“ oder „HeaderFooter“ sind.
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

### Siehe auch

* enum [NodeType](../../nodetype/)
* class [HeaderFooter](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
