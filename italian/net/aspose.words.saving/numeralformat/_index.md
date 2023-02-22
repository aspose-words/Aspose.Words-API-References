---
title: Enum NumeralFormat
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.NumeralFormat enum. Indica il set di simboli utilizzato per rappresentare i numeri durante il rendering in formati di pagina fissi.
type: docs
weight: 5030
url: /it/net/aspose.words.saving/numeralformat/
---
## NumeralFormat enumeration

Indica il set di simboli utilizzato per rappresentare i numeri durante il rendering in formati di pagina fissi.

```csharp
public enum NumeralFormat
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| European | `0` | Numeri europei: 0123456789. |
| ArabicIndic | `1` | Numeri usati in arabo: ٠١٢٣٤٥٦٧٨٩. Intervallo Unicode U+0660 - u+0669. |
| EasternArabicIndic | `2` | Numeri utilizzati in persiano e urdu: ۰۱۲۳۴۵۶۷۸۹. Intervallo Unicode U+06F0 - u+06F9. |
| Context | `3` | Il set di simboli è deciso dal contesto (proprietà locale e RTL). |
| System | `4` | QUESTA OPZIONE NON È SUPPORTATA. Il set di simboli è deciso dalle impostazioni regionali. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


