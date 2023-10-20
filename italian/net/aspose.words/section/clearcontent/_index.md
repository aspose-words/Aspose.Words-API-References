---
title: Section.ClearContent
linktitle: ClearContent
articleTitle: ClearContent
second_title: Aspose.Words per .NET
description: Section ClearContent metodo. Cancella la sezione in C#.
type: docs
weight: 90
url: /it/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

Cancella la sezione.

```csharp
public void ClearContent()
```

## Osservazioni

Il testo di[`Body`](../body/) viene cancellato, rimane solo un paragrafo vuoto che rappresenta l'interruzione di sezione.

Il testo di tutte le intestazioni e piè di pagina viene cancellato, ma[`HeaderFooter`](../../headerfooter/) gli oggetti stessi non vengono rimossi.

## Esempi

Mostra come cancellare il contenuto di una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// L'esecuzione del metodo "ClearContent" rimuoverà tutto il contenuto della sezione
// ma lascia un paragrafo vuoto per aggiungere nuovamente contenuto.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### Guarda anche

* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
