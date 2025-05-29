---
title: Node.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words für .NET
description: Duplizieren Sie Knoten mühelos mit der Node-Clone-Methode. Verbessern Sie Ihren Entwicklungsprozess und steigern Sie die Projekteffizienz noch heute!
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
| isCloneChildren | Boolean | „True“, um den Teilbaum unter dem angegebenen Knoten rekursiv zu klonen; „ false“, um nur den Knoten selbst zu klonen. |

### Rückgabewert

Der geklonte Knoten.

## Bemerkungen

Diese Methode dient als Kopierkonstruktor für Knoten. Der geklonte Knoten hat keinen übergeordneten Knoten, gehört aber zum selben Dokument wie der ursprüngliche Knoten.

Diese Methode führt immer eine vollständige Kopie des Knotens durch. Die*isCloneChildren* parameter gibt an, ob auch alle untergeordneten Knoten kopiert werden sollen.

## Beispiele

Zeigt, wie ein zusammengesetzter Knoten geklont wird.

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;
para.AppendChild(new Run(doc, "Hello world!"));

// Unten sind zwei Möglichkeiten zum Klonen eines zusammengesetzten Knotens aufgeführt.
// 1 – Erstellen Sie einen Klon eines Knotens und erstellen Sie auch einen Klon jedes seiner untergeordneten Knoten.
Node cloneWithChildren = para.Clone(true);

Assert.IsTrue(((CompositeNode)cloneWithChildren).HasChildNodes);
Assert.AreEqual("Hello world!", cloneWithChildren.GetText().Trim());

// 2 – Erstellen Sie einen Klon eines Knotens allein ohne untergeordnete Elemente.
Node cloneWithoutChildren = para.Clone(false);

Assert.IsFalse(((CompositeNode)cloneWithoutChildren).HasChildNodes);
Assert.AreEqual(string.Empty, cloneWithoutChildren.GetText().Trim());
```

### Siehe auch

* class [Node](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
