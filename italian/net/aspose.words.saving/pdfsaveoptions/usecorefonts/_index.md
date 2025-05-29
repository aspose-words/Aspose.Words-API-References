---
title: PdfSaveOptions.UseCoreFonts
linktitle: UseCoreFonts
articleTitle: UseCoreFonts
second_title: Aspose.Words per .NET
description: Ottimizza i tuoi PDF con PdfSaveOptions! Controlla la sostituzione dei font TrueType come Arial e Times New Roman per migliorare la qualità del documento.
type: docs
weight: 330
url: /it/net/aspose.words.saving/pdfsaveoptions/usecorefonts/
---
## PdfSaveOptions.UseCoreFonts property

Ottiene o imposta un valore che determina se sostituire o meno i font TrueType Arial, Times New Roman, Courier New e Symbol con i font PDF Type 1 principali.

```csharp
public bool UseCoreFonts { get; set; }
```

## Osservazioni

Il valore predefinito è`falso` Quando questo valore è impostato su`VERO` I font Arial, Times New Roman, Courier New e Symbol vengono sostituiti nel documento PDF con il font Type 1 principale corrispondente.

I font PDF principali, ovvero le relative metriche e i font sostitutivi adatti, devono essere disponibili per qualsiasi applicazione di visualizzazione PDF.

Questa impostazione funziona solo per il testo con codifica ANSI (Windows-1252). Il testo non ANSI verrà scritto con il font TrueType incorporato, indipendentemente da questa impostazione.

Per essere conformi agli standard PDF/A e PDF/UA, tutti i font devono essere incorporati.`falso` il valore verrà utilizzato automaticamente durante il salvataggio in formato PDF/A e PDF/UA.

I font principali non sono supportati durante il salvataggio in formato PDF 2.0.`falso` il valore verrà utilizzato automaticamente durante il salvataggio in PDF 2.0.

Questa opzione ha una priorità più alta quindi[`FontEmbeddingMode`](../fontembeddingmode/) opzione.

## Esempi

Mostra come abilitare/disabilitare la sostituzione del font PDF Type 1.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Courier New";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();
// Imposta la proprietà "UseCoreFonts" su "true" per sostituire alcuni font,
// inclusi i due font presenti nel nostro documento, con i loro equivalenti PDF Type 1.
// Impostare la proprietà "UseCoreFonts" su "false" per non applicare i font PDF Type 1.
options.UseCoreFonts = useCoreFonts;

doc.Save(ArtifactsDir + "PdfSaveOptions.EmbedCoreFonts.pdf", options);
```

### Guarda anche

* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
