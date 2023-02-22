---
title: Node.NodeTypeToString
second_title: Aspose.Words für .NET-API-Referenz
description: Node methode. Eine Dienstprogrammmethode die einen Aufzählungswert eines Knotentyps in eine benutzerfreundliche Zeichenfolge umwandelt.
type: docs
weight: 170
url: /de/net/aspose.words/node/nodetypetostring/
---
## Node.NodeTypeToString method

Eine Dienstprogrammmethode, die einen Aufzählungswert eines Knotentyps in eine benutzerfreundliche Zeichenfolge umwandelt.

```csharp
public static string NodeTypeToString(NodeType nodeType)
```

### Beispiele

Zeigt, wie die NextSibling-Eigenschaft eines Knotens verwendet wird, um seine unmittelbar untergeordneten Elemente aufzuzählen.

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

Zeigt, wie die Baumstruktur untergeordneter Knoten eines zusammengesetzten Knotens durchlaufen wird.

```csharp
{
    Document doc = new Document(MyDir + "Paragraphs.docx");

    // Jeder Knoten, der untergeordnete Knoten enthalten kann, wie z. B. das Dokument selbst, ist zusammengesetzt.
    Assert.True(doc.IsComposite);

    // Rufen Sie die rekursive Funktion auf, die alle untergeordneten Knoten eines zusammengesetzten Knotens durchläuft und ausgibt.
    TraverseAllNodes(doc, 0);
}

/// <summary>
/// Durchläuft rekursiv einen Knotenbaum, während der Typ jedes Knotens ausgegeben wird
/// mit einem Einzug in Abhängigkeit von der Tiefe sowie den Inhalten aller Inline-Knoten.
/// </summary>
public void TraverseAllNodes(CompositeNode parentNode, int depth)
{
    for (Node childNode = parentNode.FirstChild; childNode != null; childNode = childNode.NextSibling)
    {
        Console.Write($"{new string('\t', depth)}{Node.NodeTypeToString(childNode.NodeType)}");

        // Rekursion in den Knoten, wenn es sich um einen zusammengesetzten Knoten handelt. Geben Sie andernfalls seinen Inhalt aus, wenn es sich um einen Inline-Knoten handelt.
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
* namensraum [Aspose.Words](../../node/)
* Montage [Aspose.Words](../../../)


