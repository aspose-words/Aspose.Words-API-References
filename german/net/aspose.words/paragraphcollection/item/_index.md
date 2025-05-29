---
title: ParagraphCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words für .NET
description: Greifen Sie mit der ParagraphCollection-Elementeigenschaft einfach auf bestimmte Absätze zu. Rufen Sie beliebige Absätze nach Index ab, um eine nahtlose Textverwaltung zu ermöglichen.
type: docs
weight: 10
url: /de/net/aspose.words/paragraphcollection/item/
---
## ParagraphCollection indexer

Ruft eine[`Paragraph`](../../paragraph/) am angegebenen Index.

```csharp
public Paragraph this[int index] { get; }
```

| Parameter | Beschreibung |
| --- | --- |
| index | Ein Index zur Sammlung. |

## Bemerkungen

Der Index ist nullbasiert.

Negative Indizes sind zulässig und zeigen den Zugriff vom Ende der Sammlung an. Beispielsweise bedeutet -1 das letzte Element, -2 das vorletzte und so weiter.

Wenn der Index größer oder gleich der Anzahl der Elemente in der Liste ist, wird eine Nullreferenz zurückgegeben.

Wenn der Index negativ ist und sein absoluter Wert größer als die Anzahl der Elemente in der Liste ist, wird eine Nullreferenz zurückgegeben.

## Beispiele

Zeigt, wie überprüft wird, ob es sich bei einem Absatz um eine verschobene Revision handelt.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Dieses Dokument enthält „Verschieben“-Revisionen, die erscheinen, wenn wir Text mit dem Cursor markieren,
// und ziehen Sie es dann, um es an eine andere Position zu verschieben
// während Sie Revisionen in Microsoft Word über „Überprüfen“ -> „Änderungen nachverfolgen“ verfolgen.
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

    // Das Verschieben von Revisionen besteht aus Paaren von „Verschieben von“ und „Verschieben nach“-Revisionen.
// Diese Revisionen sind mögliche Änderungen am Dokument, die wir entweder akzeptieren oder ablehnen können.
// Bevor wir eine Verschiebungsrevision akzeptieren/ablehnen, muss das Dokument
// muss sowohl das Abfahrts- als auch das Ankunftsziel des Textes im Auge behalten.
// Der zweite und der vierte Absatz definieren eine solche Revision und haben daher beide denselben Inhalt.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// Die Revision „Verschieben von“ ist der Absatz, aus dem wir den Text gezogen haben.
// Wenn wir die Überarbeitung akzeptieren, verschwindet dieser Absatz,
// und das andere bleibt bestehen und ist keine Revision mehr.
Assert.True(paragraphs[1].IsMoveFromRevision);

// Die Revision „Verschieben nach“ ist der Absatz, in den wir den Text gezogen haben.
// Wenn wir die Überarbeitung ablehnen, verschwindet stattdessen dieser Absatz und der andere bleibt bestehen.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Siehe auch

* class [Paragraph](../../paragraph/)
* class [ParagraphCollection](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
