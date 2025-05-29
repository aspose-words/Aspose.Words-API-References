---
title: CommentRangeStart.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CommentRangeStart NodeType, som effektivt hämtar startpunkten för kommentarer för förbättrad datahantering.
type: docs
weight: 30
url: /sv/net/aspose.words/commentrangestart/nodetype/
---
## CommentRangeStart.NodeType property

ReturerCommentRangeStart .

```csharp
public override NodeType NodeType { get; }
```

## Exempel

Visar hur man går igenom en sammansatt nods träd av undernoder.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Alla noder som kan innehålla undernoder, såsom själva dokumentet, är sammansatta.
    Assert.True(doc.IsComposite);

    // Anropa den rekursiva funktionen som går igenom och skriver ut alla undernoder till en sammansatt nod.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Går rekursivt igenom ett nodträd samtidigt som typen för varje nod skrivs ut
/// med ett indrag beroende på djup samt innehållet i alla inline-noder.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Rekursiv in i noden om det är en sammansatt nod. Annars, skriv ut dess innehåll om det är en inline-nod.
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

### Se även

* enum [NodeType](../../nodetype/)
* class [CommentRangeStart](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
