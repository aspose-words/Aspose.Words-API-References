---
title: CompositeNode.IsComposite
linktitle: IsComposite
articleTitle: IsComposite
second_title: Aspose.Words för .NET
description: Upptäck egenskapen CompositeNode IsComposite. Kontrollera enkelt om en nod stöder underordnade noder för förbättrad hantering av datastrukturer.
type: docs
weight: 40
url: /sv/net/aspose.words/compositenode/iscomposite/
---
## CompositeNode.IsComposite property

Returer`sann` eftersom denna nod kan ha underordnade noder.

```csharp
public override bool IsComposite { get; }
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

* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
