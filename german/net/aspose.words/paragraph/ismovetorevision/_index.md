---
title: Paragraph.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words für .NET
description: Entdecken Sie die IsMoveToRevision-Eigenschaft in Microsoft Word! Erfahren Sie, wie sie Änderungen verfolgt und Ihre Dokumentbearbeitung verbessert.
type: docs
weight: 140
url: /de/net/aspose.words/paragraph/ismovetorevision/
---
## Paragraph.IsMoveToRevision property

Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war.

```csharp
public bool IsMoveToRevision { get; }
```

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

* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
