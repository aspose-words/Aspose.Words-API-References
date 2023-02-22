---
title: FixedPageSaveOptions.NumeralFormat
second_title: Aspose.Words per .NET API Reference
description: FixedPageSaveOptions proprietà. Ottiene o impostaNumeralFormat utilizzato per il rendering dei numeri. I numeri europei vengono utilizzati per impostazione predefinita.
type: docs
weight: 40
url: /it/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

Ottiene o imposta[`NumeralFormat`](../../numeralformat/) utilizzato per il rendering dei numeri. I numeri europei vengono utilizzati per impostazione predefinita.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

### Osservazioni

Se il valore di questa proprietà viene modificato e il layout di pagina è già creato, allora [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) viene richiamato automaticamente per aggiornare eventuali modifiche.

### Esempi

Mostra come impostare il formato numerico utilizzato durante il salvataggio in PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "NumeralFormat" su "NmeralFormat.ArabicIndic" su
// usa i glifi dall'intervallo U+0660 a U+0669 come numeri.
// Imposta la proprietà "NmeralFormat" su "NmeralFormat.Context" su
// cerca la localizzazione per determinare il numero di glifi da usare.
// Imposta la proprietà "NumeralFormat" su "NumeralFormat.EasternArabicIndic" su
// usa i glifi dall'intervallo U+06F0 a U+06F9 come numeri.
// Imposta la proprietà "NumeralFormat" su "NmeralFormat.European" per utilizzare i numeri europei.
// Impostare la proprietà "NmeralFormat" su "NmeralFormat.System" per determinare il set di simboli dalle impostazioni internazionali.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Guarda anche

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../fixedpagesaveoptions/)
* assemblea [Aspose.Words](../../../)


