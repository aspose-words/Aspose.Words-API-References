---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: Aspose.Words per .NET
description: Section ClearHeadersFooters metodo. Cancella le intestazioni e i piè di pagina di questa sezione in C#.
type: docs
weight: 100
url: /it/net/aspose.words/section/clearheadersfooters/
---
## Section.ClearHeadersFooters method

Cancella le intestazioni e i piè di pagina di questa sezione.

```csharp
public void ClearHeadersFooters()
```

## Osservazioni

Il testo di tutte le intestazioni e piè di pagina viene cancellato, ma[`HeaderFooter`](../../headerfooter/) gli oggetti stessi non vengono rimossi.

Ciò rende le intestazioni e i piè di pagina di questa sezione collegati alle intestazioni e ai piè di pagina della sezione precedente.

## Esempi

Mostra come cancellare il contenuto di tutte le intestazioni e i piè di pagina in una sezione.

```csharp
Document doc = new Document();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters.Count);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the primary header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the primary footer.");

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual("This is the primary header.", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("This is the primary footer.", doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Svuota tutte le intestazioni e i piè di pagina di questa sezione da tutto il loro contenuto.
// Le intestazioni e i piè di pagina saranno ancora presenti ma non avranno nulla da visualizzare.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### Guarda anche

* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
