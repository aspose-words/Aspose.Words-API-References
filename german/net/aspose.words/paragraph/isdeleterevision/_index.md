---
title: Paragraph.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „IsDeleteRevision“ in Microsoft Word. Erfahren Sie, wie sie Löschungen während der Änderungsverfolgung für ein effizientes Dokumentenmanagement anzeigt.
type: docs
weight: 40
url: /de/net/aspose.words/paragraph/isdeleterevision/
---
## Paragraph.IsDeleteRevision property

Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war.

```csharp
public bool IsDeleteRevision { get; }
```

## Beispiele

Zeigt, wie mit Revisionsabsätzen gearbeitet wird.

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// Die obigen Absätze sind keine Überarbeitungen.
// Absätze, die wir nach dem Starten der Revisionsverfolgung hinzufügen, werden als „Einfügen“-Revisionen registriert.
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// Absätze, die wir nach dem Starten der Revisionsverfolgung entfernen, werden als „Gelöschte“ Revisionen registriert.
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// Solche Absätze bleiben bestehen, bis wir die Löschrevision entweder akzeptieren oder ablehnen.
// Durch die Annahme der Überarbeitung wird der Absatz endgültig entfernt.
// und wenn Sie die Revision ablehnen, bleibt sie im Dokument, als hätten wir sie nie gelöscht.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// Akzeptieren Sie die Überarbeitung und überprüfen Sie dann, ob der Absatz verschwunden ist.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.AreEqual(0, para.Count);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### Siehe auch

* class [Paragraph](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
