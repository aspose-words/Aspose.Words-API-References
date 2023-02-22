---
title: BookmarkStart.NodeType
second_title: Aspose.Words för .NET API Referens
description: BookmarkStart fast egendom. ReturnerarBookmarkStart .
type: docs
weight: 40
url: /sv/net/aspose.words/bookmarkstart/nodetype/
---
## BookmarkStart.NodeType property

ReturnerarBookmarkStart .

```csharp
public override NodeType NodeType { get; }
```

### Exempel

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

* enum [NodeType](../../nodetype/)
* class [BookmarkStart](../)
* namnutrymme [Aspose.Words](../../bookmarkstart/)
* hopsättning [Aspose.Words](../../../)


