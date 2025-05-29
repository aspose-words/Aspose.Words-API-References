---
title: SmartTag.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words für .NET
description: Entdecken Sie die SmartTag NodeType-Eigenschaft, die Ihre Inhalte mit dynamischen Tagging-Funktionen erweitert. Profitieren Sie von nahtloser Integration und steigern Sie das Benutzerengagement!
type: docs
weight: 30
url: /de/net/aspose.words.markup/smarttag/nodetype/
---
## SmartTag.NodeType property

RückgabenSmartTag .

```csharp
public override NodeType NodeType { get; }
```

## Beispiele

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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [SmartTag](../)
* namensraum [Aspose.Words.Markup](../../../aspose.words.markup/)
* Montage [Aspose.Words](../../../)
