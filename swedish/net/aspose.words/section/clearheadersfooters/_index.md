---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: Aspose.Words för .NET
description: Rensa enkelt avsnittshuvuden och sidfot med metoden ClearHeadersFooters. Effektivisera din dokumentlayout för ett elegant utseende!
type: docs
weight: 120
url: /sv/net/aspose.words/section/clearheadersfooters/
---
## ClearHeadersFooters() {#clearheadersfooters}

Rensar sidhuvuden och sidfoten i det här avsnittet.

```csharp
public void ClearHeadersFooters()
```

## Anmärkningar

Texten i alla sidhuvuden och sidfot rensas, men[`HeaderFooter`](../../headerfooter/) själva föremålen tas inte bort.

Detta länkar sidhuvuden och sidfoten i det här avsnittet till sidhuvuden och sidfoten i föregående avsnitt.

## Exempel

Visar hur man rensar innehållet i alla sidhuvuden och sidfot i ett avsnitt.

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

// Töm alla sidhuvuden och sidfot i det här avsnittet på allt innehåll.
// Sidhuvuden och sidfoten kommer fortfarande att finnas kvar men det kommer inte att finnas något att visa.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### Se även

* class [Section](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## ClearHeadersFooters(*bool*) {#clearheadersfooters_1}

Rensar sidhuvuden och sidfoten i det här avsnittet.

```csharp
public void ClearHeadersFooters(bool preserveWatermarks)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| preserveWatermarks | Boolean | Sant om vattenstämplarna inte ska tas bort. |

## Anmärkningar

Texten i alla sidhuvuden och sidfot rensas, men[`HeaderFooter`](../../headerfooter/) själva föremålen tas inte bort.

Detta länkar sidhuvuden och sidfoten i det här avsnittet till sidhuvuden och sidfoten i föregående avsnitt.

## Exempel

Visar hur man rensar innehållet i sidhuvud och sidfot med eller utan vattenstämpel.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Lägg till ett vattenmärke i vanlig text.
doc.Watermark.SetText("Aspose Watermark");

// Se till att sidhuvuden och sidfoten har innehåll.
HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("First header", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("Second header", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("Third header", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("First footer", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("Second footer", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("Third footer", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Tar bort allt innehåll i sidhuvud och sidfot förutom vattenstämplar.
doc.FirstSection.ClearHeadersFooters(true);

headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
Assert.AreEqual(WatermarkType.Text, doc.Watermark.Type);

// Tar bort allt innehåll i sidhuvud och sidfot, inklusive vattenstämplar.
doc.FirstSection.ClearHeadersFooters(false);
Assert.AreEqual(WatermarkType.None, doc.Watermark.Type);
```

### Se även

* class [Section](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
