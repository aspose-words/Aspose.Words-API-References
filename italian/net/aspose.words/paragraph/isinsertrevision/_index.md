---
title: Paragraph.IsInsertRevision
second_title: Aspose.Words per .NET API Reference
description: Paragraph proprietà. Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre era abilitato il rilevamento delle modifiche.
type: docs
weight: 110
url: /it/net/aspose.words/paragraph/isinsertrevision/
---
## Paragraph.IsInsertRevision property

Restituisce true se questo oggetto è stato inserito in Microsoft Word mentre era abilitato il rilevamento delle modifiche.

```csharp
public bool IsInsertRevision { get; }
```

### Esempi

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

// Tali paragrafi rimarranno fino a quando non accettiamo o rifiutiamo la revisione dell'eliminazione.
// L'accettazione della revisione rimuoverà definitivamente il paragrafo,
// e rifiutando la revisione la lascerà nel documento come se non l'avessimo mai cancellata.
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
* spazio dei nomi [Aspose.Words](../../paragraph/)
* assemblea [Aspose.Words](../../../)


