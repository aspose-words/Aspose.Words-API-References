---
title: Node.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words für .NET
description: Node Clone methode. Erstellt ein Duplikat des Knotens in C#.
type: docs
weight: 100
url: /de/net/aspose.words/node/clone/
---
## Node.Clone method

Erstellt ein Duplikat des Knotens.

```csharp
public Node Clone(bool isCloneChildren)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| isCloneChildren | Boolean | True, um den Teilbaum rekursiv unter dem angegebenen Knoten zu klonen; false, um nur den Knoten selbst zu klonen. |

### Rückgabewert

Der geklonte Knoten.

## Bemerkungen

Diese Methode dient als Kopierkonstruktor für Knoten. Der geklonte Knoten hat keinen übergeordneten Knoten, gehört aber zum selben Dokument wie der ursprüngliche Knoten.

Diese Methode führt immer eine tiefe Kopie des Knotens durch. Der*isCloneChildren* parameter gibt an, ob auch alle untergeordneten Knoten kopiert werden sollen.

## Beispiele

Zeigt, wie ein zusammengesetzter Knoten geklont wird.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Nachfolgend finden Sie zwei Möglichkeiten zum Klonen eines zusammengesetzten Knotens.
// 1 – Erstellen Sie einen Klon eines Knotens und erstellen Sie auch einen Klon jedes seiner untergeordneten Knoten.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 – Erstellen Sie einen Klon eines einzelnen Knotens ohne untergeordnete Elemente.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### Siehe auch

* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
