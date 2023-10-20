---
title: Paragraph.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words per .NET
description: Paragraph IsDeleteRevision proprietà. Restituisce vero se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche in C#.
type: docs
weight: 40
url: /it/net/aspose.words/paragraph/isdeleterevision/
---
## Paragraph.IsDeleteRevision property

Restituisce vero se questo oggetto è stato eliminato in Microsoft Word mentre era abilitato il rilevamento delle modifiche.

```csharp
public bool IsDeleteRevision { get; }
```

## Esempi

Mostra come lavorare con i paragrafi di revisione.

```csharp
Document doc = new Document();
Body body = doc.FirstSection.Body;
Paragraph para = body.FirstParagraph;

para.AppendChild(new Run(doc, "Paragraph 1. "));
body.AppendParagraph("Paragraph 2. ");
body.AppendParagraph("Paragraph 3. ");

// I paragrafi precedenti non sono revisioni.
// I paragrafi che aggiungiamo dopo aver avviato il monitoraggio delle revisioni verranno registrati come revisioni "Inserisci".
doc.StartTrackRevisions("John Doe", DateTime.Now);

para = body.AppendParagraph("Paragraph 4. ");

Assert.True(para.IsInsertRevision);

// I paragrafi che rimuoviamo dopo aver avviato il monitoraggio delle revisioni verranno registrati come revisioni "Elimina".
ParagraphCollection paragraphs = body.Paragraphs;

Assert.AreEqual(4, paragraphs.Count);

para = paragraphs[2];
para.Remove();

// Tali paragrafi rimarranno finché non accetteremo o rifiuteremo la revisione di eliminazione.
// Accettare la revisione rimuoverà definitivamente il paragrafo,
// e rifiutando la revisione la lasceremo nel documento come se non l'avessimo mai cancellata.
Assert.AreEqual(4, paragraphs.Count);
Assert.True(para.IsDeleteRevision);

// Accetta la revisione, quindi verifica che il paragrafo sia scomparso.
doc.AcceptAllRevisions();

Assert.AreEqual(3, paragraphs.Count);
Assert.That(para, Is.Empty);
Assert.AreEqual(
    "Paragraph 1. \r" +
    "Paragraph 2. \r" +
    "Paragraph 4.", doc.GetText().Trim());
```

### Guarda anche

* class [Paragraph](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
