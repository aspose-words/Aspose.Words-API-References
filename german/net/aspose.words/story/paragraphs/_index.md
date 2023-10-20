---
title: Story.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words für .NET
description: Story Paragraphs eigendom. Ruft eine Sammlung von Absätzen ab die unmittelbar untergeordnete Elemente der Geschichte sind in C#.
type: docs
weight: 30
url: /de/net/aspose.words/story/paragraphs/
---
## Story.Paragraphs property

Ruft eine Sammlung von Absätzen ab, die unmittelbar untergeordnete Elemente der Geschichte sind.

```csharp
public ParagraphCollection Paragraphs { get; }
```

## Beispiele

Zeigt, wie überprüft wird, ob es sich bei einem Absatz um eine Verschiebungsrevision handelt.

```csharp
Document doc = new Document(MyDir + "Revisions.docx");

// Dieses Dokument enthält „Verschieben“-Revisionen, die angezeigt werden, wenn wir Text mit dem Cursor markieren.
// und ziehen Sie es dann, um es an eine andere Position zu verschieben
// während Überarbeitungen in Microsoft Word über „Überprüfen“ verfolgt werden -> "Änderungen verfolgen".
Assert.AreEqual(6, doc.Revisions.Count(r => r.RevisionType == RevisionType.Moving));

ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

 // Verschieberevisionen bestehen aus Paaren von „Verschieben von“- und „Verschieben nach“-Revisionen.
// Bei diesen Überarbeitungen handelt es sich um potenzielle Änderungen am Dokument, die wir entweder akzeptieren oder ablehnen können.
// Bevor wir eine Verschiebungsrevision akzeptieren/ablehnen, das Dokument
// muss sowohl das Abflug- als auch das Ankunftsziel des Textes im Auge behalten.
// Der zweite und der vierte Absatz definieren eine solche Revision und haben daher beide den gleichen Inhalt.
Assert.AreEqual(paragraphs[1].GetText(), paragraphs[3].GetText());

// Die Revision „Verschieben von“ ist der Absatz, aus dem wir den Text gezogen haben.
// Wenn wir die Überarbeitung akzeptieren, wird dieser Absatz verschwinden,
// und der andere bleibt bestehen und ist keine Revision mehr.
Assert.True(paragraphs[1].IsMoveFromRevision);

// Die „Verschieben nach“-Revision ist der Absatz, in den wir den Text gezogen haben.
// Wenn wir die Überarbeitung ablehnen, verschwindet stattdessen dieser Absatz und der andere bleibt bestehen.
Assert.True(paragraphs[3].IsMoveToRevision);
```

### Siehe auch

* class [ParagraphCollection](../../paragraphcollection/)
* class [Story](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
