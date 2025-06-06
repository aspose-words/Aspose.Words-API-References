---
title: Node.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words für .NET
description: Entdecken Sie die Methode „Node Remove“, um Knoten mühelos von ihrem übergeordneten Element zu trennen und so die Effizienz und Struktur Ihres Codes zu verbessern.
type: docs
weight: 150
url: /de/net/aspose.words/node/remove/
---
## Node.Remove method

Entfernt sich selbst vom übergeordneten Element.

```csharp
public void Remove()
```

## Beispiele

Zeigt, wie alle Formen mit Bildern aus einem Dokument gelöscht werden.

```csharp
Document doc = new Document(MyDir + "Images.docx");
NodeCollection shapes = doc.GetChildNodes(NodeType.Shape, true);

Assert.AreEqual(9, shapes.OfType<Shape>().Count(s => s.HasImage));

foreach (Shape shape in shapes.OfType<Shape>())
    if (shape.HasImage) 
        shape.Remove();

Assert.AreEqual(0, shapes.OfType<Shape>().Count(s => s.HasImage));
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

### Siehe auch

* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
