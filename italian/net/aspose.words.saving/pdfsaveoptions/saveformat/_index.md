---
title: PdfSaveOptions.SaveFormat
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions proprietà. Specifica il formato in cui verrà salvato il documento se viene utilizzato questo oggetto opzioni di salvataggio. Può esserePdf .
type: docs
weight: 250
url: /it/net/aspose.words.saving/pdfsaveoptions/saveformat/
---
## PdfSaveOptions.SaveFormat property

Specifica il formato in cui verrà salvato il documento se viene utilizzato questo oggetto opzioni di salvataggio. Può esserePdf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

### Esempi

Mostra come limitare il livello delle intestazioni che appariranno nella struttura di un documento PDF salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce intestazioni che possono fungere da voci TOC di livello 1, 2 e poi 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Il documento PDF di output conterrà uno schema, ovvero un sommario che elenca le intestazioni nel corpo del documento.
// Cliccando su una voce in questo schema ci porterà alla posizione della rispettiva intestazione.
// Imposta la proprietà "HeadingsOutlineLevels" su "2" per escludere tutte le intestazioni i cui livelli sono superiori a 2 dalla struttura.
// Le ultime due intestazioni che abbiamo inserito sopra non appariranno.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

### Guarda anche

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


