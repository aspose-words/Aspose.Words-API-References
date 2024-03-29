---
title: BuildingBlock.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words für .NET
description: BuildingBlock NodeType eigendom. Gibt die zurückBuildingBlock value in C#.
type: docs
weight: 100
url: /de/net/aspose.words.buildingblocks/buildingblock/nodetype/
---
## BuildingBlock.NodeType property

Gibt die zurückBuildingBlock value.

```csharp
public override NodeType NodeType { get; }
```

## Beispiele

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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [BuildingBlock](../)
* namensraum [Aspose.Words.BuildingBlocks](../../../aspose.words.buildingblocks/)
* Montage [Aspose.Words](../../../)
