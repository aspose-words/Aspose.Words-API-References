---
title: FixedPageSaveOptions.NumeralFormat
linktitle: NumeralFormat
articleTitle: NumeralFormat
second_title: Aspose.Words per .NET
description: FixedPageSaveOptions NumeralFormat proprietà. Ottiene o impostaNumeralFormat utilizzato per il rendering dei numeri. I numeri europei vengono utilizzati per impostazione predefinita in C#.
type: docs
weight: 40
url: /it/net/aspose.words.saving/fixedpagesaveoptions/numeralformat/
---
## FixedPageSaveOptions.NumeralFormat property

Ottiene o imposta[`NumeralFormat`](../../numeralformat/) utilizzato per il rendering dei numeri. I numeri europei vengono utilizzati per impostazione predefinita.

```csharp
public NumeralFormat NumeralFormat { get; set; }
```

## Osservazioni

Se il valore di questa proprietà viene modificato e il layout della pagina è già creato, allora [`UpdatePageLayout`](../../../aspose.words/document/updatepagelayout/) viene richiamato automaticamente per aggiornare eventuali modifiche.

## Esempi

Mostra come impostare il formato numerico utilizzato durante il salvataggio in PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.LocaleId = new CultureInfo("ar-AR").LCID;
builder.Writeln("1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 50, 100");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "NumeralFormat" su "NumeralFormat.ArabicIndic" su
// usa i glifi dall'intervallo da U+0660 a U+0669 come numeri.
// Imposta la proprietà "NumeralFormat" su "NumeralFormat.Context" su
// cerca la locale per determinare quale numero di glifi utilizzare.
// Imposta la proprietà "NumeralFormat" su "NumeralFormat.EasternArabicIndic" su
// usa i glifi dall'intervallo da U+06F0 a U+06F9 come numeri.
// Imposta la proprietà "NumeralFormat" su "NumeralFormat.European" per utilizzare i numeri europei.
// Imposta la proprietà "NumeralFormat" su "NumeralFormat.System" per determinare il set di simboli dalle impostazioni regionali.
options.NumeralFormat = numeralFormat;

doc.Save(ArtifactsDir + "PdfSaveOptions.SetNumeralFormat.pdf", options);
```

### Guarda anche

* enum [NumeralFormat](../../numeralformat/)
* class [FixedPageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
