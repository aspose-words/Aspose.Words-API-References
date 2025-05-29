---
title: Node.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words für .NET
description: Entdecken Sie die NodeType-Eigenschaft von Node, um Knotentypen in Ihrer Anwendung einfach zu identifizieren und so Ihre Entwicklungseffizienz und Codeübersichtlichkeit zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words/node/nodetype/
---
## Node.NodeType property

Ruft den Typ dieses Knotens ab.

```csharp
public abstract NodeType NodeType { get; }
```

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

Zeigt, wie alle untergeordneten Knoten eines bestimmten Typs aus einem zusammengesetzten Knoten entfernt werden.

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Assert.AreEqual(2, doc.GetChildNodes(NodeType.Table, true).Count);

Node curNode = doc.FirstSection.Body.FirstChild;

while (curNode != null)
{
    // Speichern Sie den nächsten Geschwisterknoten als Variable, falls wir nach dem Löschen dieses Knotens dorthin wechseln möchten.
    Node nextNode = curNode.NextSibling;

    // Ein Abschnittstext kann Absatz- und Tabellenknoten enthalten.
    // Wenn der Knoten eine Tabelle ist, entfernen Sie ihn vom übergeordneten Knoten.
    if (curNode.NodeType == NodeType.Table)
        curNode.Remove();

    curNode = nextNode;
}

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Table, true).Count);
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

* enum [NodeType](../../nodetype/)
* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
