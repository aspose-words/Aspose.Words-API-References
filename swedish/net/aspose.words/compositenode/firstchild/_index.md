---
title: CompositeNode.FirstChild
second_title: Aspose.Words för .NET API Referens
description: CompositeNode fast egendom. Får det första barnet i noden.
type: docs
weight: 30
url: /sv/net/aspose.words/compositenode/firstchild/
---
## CompositeNode.FirstChild property

Får det första barnet i noden.

```csharp
public Node FirstChild { get; }
```

### Anmärkningar

Om det inte finns någon första underordnad nod, returneras en noll.

### Exempel

Visar hur man använder en nods NextSibling-egenskap för att räkna upp sina närmaste barn.

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

Visar hur man korsar en sammansatt nods träd med undernoder.

```csharp
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Alla noder som kan innehålla underordnade noder, till exempel själva dokumentet, är sammansatta.
    Assert.True(doc.IsComposite);

    // Anropa den rekursiva funktionen som kommer att gå igenom och skriva ut alla undernoder för en sammansatt nod.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Går rekursivt genom ett nodträd medan du skriver ut typen av varje nod
/// med ett indrag beroende på djup samt innehållet i alla inline-noder.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Gå tillbaka in i noden om det är en sammansatt nod. Annars skriv ut dess innehåll om det är en inline-nod.
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

* class [Node](../../node/)
* class [CompositeNode](../)
* namnutrymme [Aspose.Words](../../compositenode/)
* hopsättning [Aspose.Words](../../../)


