---
title: Node.NodeTypeToString
linktitle: NodeTypeToString
articleTitle: NodeTypeToString
second_title: Aspose.Words för .NET
description: Upptäck Node NodeTypeToString-metoden, konvertera enkelt nodtypsuppräkningar till användarvänliga strängar för sömlös kodning och förbättrad läsbarhet.
type: docs
weight: 170
url: /sv/net/aspose.words/node/nodetypetostring/
---
## Node.NodeTypeToString method

En verktygsmetod som konverterar ett nodtypsuppräkningsvärde till en användarvänlig sträng.

```csharp
public static string NodeTypeToString(NodeType nodeType)
```

## Exempel

Visar hur man använder en nods NextSibling-egenskap för att räkna upp dess omedelbara underordnade objekt.

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
* class [Node](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
