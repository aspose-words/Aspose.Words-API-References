---
title: Body.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Body NodeType-Eigenschaft, die den Body-Inhalt effizient zurückgibt, Ihre Webentwicklungserfahrung verbessert und Ihre Projekte optimiert.
type: docs
weight: 20
url: /de/net/aspose.words/body/nodetype/
---
## Body.NodeType property

RückgabenBody .

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
* class [Body](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
