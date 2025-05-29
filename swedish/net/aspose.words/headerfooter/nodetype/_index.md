---
title: HeaderFooter.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words för .NET
description: Upptäck HeaderFooter NodeType-egenskapen som effektivt hämtar sidhuvud- och sidfotsdetaljer, vilket förbättrar din innehållsstruktur och användarupplevelse.
type: docs
weight: 50
url: /sv/net/aspose.words/headerfooter/nodetype/
---
## HeaderFooter.NodeType property

ReturerHeaderFooter .

```csharp
public override NodeType NodeType { get; }
```

## Exempel

Visar hur man itererar igenom barnen till en sammansatt nod.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// En sektion är en sammansatt nod och kan innehålla undernoder,
// men bara om dessa undernoder är av nodtypen "Body" eller "HeaderFooter".
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

### Se även

* enum [NodeType](../../nodetype/)
* class [HeaderFooter](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
