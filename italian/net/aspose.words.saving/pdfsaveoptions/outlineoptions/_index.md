---
title: PdfSaveOptions.OutlineOptions
second_title: Aspose.Words per .NET API Reference
description: PdfSaveOptions proprietà. Consente di specificare le opzioni del contorno.
type: docs
weight: 210
url: /it/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Consente di specificare le opzioni del contorno.

```csharp
public OutlineOptions OutlineOptions { get; }
```

### Osservazioni

È possibile creare contorni da intestazioni e segnalibri.

Per le intestazioni il livello di struttura è determinato dal livello di intestazione.

È possibile impostare il livello massimo di intestazione da includere nei contorni o disabilitare del tutto i contorni di intestazione.

Per i segnalibri il livello di struttura può essere impostato nelle opzioni come valore predefinito per tutti i segnalibri o come valori individuali per segnalibri particolari.

Inoltre, i contorni possono essere esportati in formato XPS utilizzando lo stesso`OutlineOptions` classe.

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

Mostra come lavorare con livelli struttura che non contengono alcuna intestazione corrispondente durante il salvataggio di un documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce intestazioni che possono fungere da voci TOC di livello 1 e 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Il documento PDF di output conterrà uno schema, ovvero un sommario che elenca le intestazioni nel corpo del documento.
// Cliccando su una voce in questo schema ci porterà alla posizione della rispettiva intestazione.
// Imposta la proprietà "HeadingsOutlineLevels" su "5" per includere tutte le intestazioni di livello 5 e inferiori nella struttura.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

 // Questo documento contiene titoli di livello 1 e 5 e nessun titolo con livelli di 2, 3 e 4.
// Il documento PDF di output tratterà i livelli di struttura 2, 3 e 4 come "mancanti".
// Imposta la proprietà "CreateMissingOutlineLevels" su "true" per includere tutti i livelli mancanti nella struttura,
// lasciando voci di struttura vuote poiché non ci sono intestazioni utilizzabili.
// Imposta la proprietà "CreateMissingOutlineLevels" su "false" per ignorare i livelli di struttura mancanti,
// e tratta le intestazioni del livello 5 dello schema come livello 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Guarda anche

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../pdfsaveoptions/)
* assemblea [Aspose.Words](../../../)


