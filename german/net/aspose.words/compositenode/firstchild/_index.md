---
title: CompositeNode.FirstChild
linktitle: FirstChild
articleTitle: FirstChild
second_title: Aspose.Words für .NET
description: Entdecken Sie die CompositeNode FirstChild-Eigenschaft, um einfach auf den ersten untergeordneten Knoten zuzugreifen, Ihre Codierungseffizienz zu verbessern und die Datenverwaltung zu vereinfachen.
type: docs
weight: 20
url: /de/net/aspose.words/compositenode/firstchild/
---
## CompositeNode.FirstChild property

Ruft das erste untergeordnete Element des Knotens ab.

```csharp
public Node FirstChild { get; }
```

## Bemerkungen

Wenn es keinen ersten untergeordneten Knoten gibt,`null` wird zurückgegeben.

## Beispiele

Zeigt, wie die NextSibling-Eigenschaft eines Knotens zum Aufzählen seiner unmittelbar untergeordneten Elemente verwendet wird.

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

Zeigt, wie der Baum der untergeordneten Knoten eines zusammengesetzten Knotens durchlaufen wird.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Jeder Knoten, der untergeordnete Knoten enthalten kann, wie z. B. das Dokument selbst, ist zusammengesetzt.
    Assert.True(doc.IsComposite);

    // Rufen Sie die rekursive Funktion auf, die alle untergeordneten Knoten eines zusammengesetzten Knotens durchläuft und druckt.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Durchläuft rekursiv einen Knotenbaum und gibt dabei den Typ jedes Knotens aus
/// mit einem Einzug, der von der Tiefe sowie dem Inhalt aller Inline-Knoten abhängt.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Rekursion in den Knoten, wenn es sich um einen zusammengesetzten Knoten handelt. Andernfalls wird der Inhalt gedruckt, wenn es sich um einen Inline-Knoten handelt.
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

### Siehe auch

* class [Node](../../node/)
* class [CompositeNode](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
