---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: Aspose.Words per .NET
description: Intestazioni e piè di pagina di sezione chiari e senza sforzo con il metodo ClearHeadersFooters. Ottimizza il layout del tuo documento per un aspetto impeccabile!
type: docs
weight: 120
url: /it/net/aspose.words/section/clearheadersfooters/
---
## ClearHeadersFooters() {#clearheadersfooters}

Cancella le intestazioni e i piè di pagina di questa sezione.

```csharp
public void ClearHeadersFooters()
```

## Osservazioni

Il testo di tutte le intestazioni e piè di pagina viene cancellato, ma[`HeaderFooter`](../../headerfooter/) gli oggetti stessi non vengono rimossi.

In questo modo le intestazioni e i piè di pagina di questa sezione vengono collegati alle intestazioni e ai piè di pagina della sezione precedente.

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

// Svuota tutte le intestazioni e i piè di pagina di questa sezione del loro contenuto.
// Le intestazioni e i piè di pagina saranno ancora presenti, ma non avranno nulla da visualizzare.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### Guarda anche

* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)

---

## ClearHeadersFooters(*bool*) {#clearheadersfooters_1}

Cancella le intestazioni e i piè di pagina di questa sezione.

```csharp
public void ClearHeadersFooters(bool preserveWatermarks)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| preserveWatermarks | Boolean | Vero se le filigrane non devono essere rimosse. |

## Osservazioni

Il testo di tutte le intestazioni e piè di pagina viene cancellato, ma[`HeaderFooter`](../../headerfooter/) gli oggetti stessi non vengono rimossi.

In questo modo le intestazioni e i piè di pagina di questa sezione vengono collegati alle intestazioni e ai piè di pagina della sezione precedente.

## Esempi

Mostra come cancellare il contenuto dell'intestazione e del piè di pagina con o senza filigrana.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Aggiungi una filigrana di testo normale.
doc.Watermark.SetText("Aspose Watermark");

// Assicurati che le intestazioni e i piè di pagina abbiano un contenuto.
HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("First header", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("Second header", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("Third header", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("First footer", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("Second footer", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("Third footer", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Rimuove tutto il contenuto dell'intestazione e del piè di pagina, ad eccezione delle filigrane.
doc.FirstSection.ClearHeadersFooters(true);

headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
Assert.AreEqual(WatermarkType.Text, doc.Watermark.Type);

// Rimuove tutto il contenuto dell'intestazione e del piè di pagina, comprese le filigrane.
doc.FirstSection.ClearHeadersFooters(false);
Assert.AreEqual(WatermarkType.None, doc.Watermark.Type);
```

### Guarda anche

* class [Section](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
