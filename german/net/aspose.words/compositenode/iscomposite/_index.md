---
title: CompositeNode.IsComposite
second_title: Aspose.Words für .NET-API-Referenz
description: CompositeNode eigendom. Gibt zurückWAHR da dieser Knoten untergeordnete Knoten haben kann.
type: docs
weight: 40
url: /de/net/aspose.words/compositenode/iscomposite/
---
## CompositeNode.IsComposite property

Gibt zurück`WAHR` da dieser Knoten untergeordnete Knoten haben kann.

```csharp
public override bool IsComposite { get; }
```

### Beispiele

Zeigt, wie der Baum der untergeordneten Knoten eines zusammengesetzten Knotens durchlaufen wird.

```csharp
public void RecurseChildren()
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Jeder Knoten, der untergeordnete Knoten enthalten kann, z. B. das Dokument selbst, ist zusammengesetzt.
    Assert.True(doc.IsComposite);

    // Rufen Sie die rekursive Funktion auf, die alle untergeordneten Knoten eines zusammengesetzten Knotens durchläuft und ausgibt.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Durchläuft rekursiv einen Knotenbaum und gibt dabei den Typ jedes Knotens aus
/// mit einem Einzug abhängig von der Tiefe sowie dem Inhalt aller Inline-Knoten.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Rekursion in den Knoten, wenn es sich um einen zusammengesetzten Knoten handelt. Andernfalls drucken Sie den Inhalt aus, wenn es sich um einen Inline-Knoten handelt.
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

* class [CompositeNode](../)
* namensraum [Aspose.Words](../../compositenode/)
* Montage [Aspose.Words](../../../)


