---
title: PdfSaveOptions.OutlineOptions
linktitle: OutlineOptions
articleTitle: OutlineOptions
second_title: Aspose.Words per .NET
description: Scopri la proprietà OutlineOptions di PdfSaveOptions per personalizzare facilmente i contorni dei tuoi PDF. Migliora la navigazione e l'usabilità dei documenti!
type: docs
weight: 240
url: /it/net/aspose.words.saving/pdfsaveoptions/outlineoptions/
---
## PdfSaveOptions.OutlineOptions property

Consente di specificare le opzioni del contorno.

```csharp
public OutlineOptions OutlineOptions { get; }
```

## Osservazioni

È possibile creare strutture a partire da titoli e segnalibri.

Per le intestazioni il livello della struttura è determinato dal livello dell'intestazione.

È possibile impostare il livello massimo di intestazione da includere nelle strutture oppure disattivare del tutto le strutture di intestazione.

Per i segnalibri, il livello di struttura può essere impostato nelle opzioni come valore predefinito per tutti i segnalibri o come valori individuali per segnalibri particolari.

Inoltre, i contorni possono essere esportati in formato XPS utilizzando lo stesso`OutlineOptions` classe.

## Esempi

Mostra come limitare il livello delle intestazioni che appariranno nella struttura di un documento PDF salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire titoli che possono fungere da voci di indice dei livelli 1, 2 e poi 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.SaveFormat = SaveFormat.Pdf;

// Il documento PDF di output conterrà una struttura, ovvero un indice che elenca le intestazioni nel corpo del documento.
// Cliccando su una voce in questo schema verremo indirizzati alla posizione della rispettiva intestazione.
// Impostare la proprietà "HeadingsOutlineLevels" su "2" per escludere dalla struttura tutte le intestazioni i cui livelli sono superiori a 2.
// Le ultime due intestazioni che abbiamo inserito sopra non verranno visualizzate.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeadingsOutlineLevels.pdf", saveOptions);
```

Mostra come lavorare con livelli di struttura che non contengono intestazioni corrispondenti quando si salva un documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire titoli che possono fungere da voci di indice dei livelli 1 e 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Il documento PDF di output conterrà una struttura, ovvero un indice che elenca le intestazioni nel corpo del documento.
// Cliccando su una voce in questo schema verremo indirizzati alla posizione della rispettiva intestazione.
// Impostare la proprietà "HeadingsOutlineLevels" su "5" per includere tutte le intestazioni dei livelli 5 e inferiori nella struttura.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Questo documento contiene titoli di livello 1 e 5 e nessun titolo di livello 2, 3 e 4.
// Il documento PDF di output tratterà i livelli di struttura 2, 3 e 4 come "mancanti".
// Imposta la proprietà "CreateMissingOutlineLevels" su "true" per includere tutti i livelli mancanti nello schema,
// lasciando le voci di riepilogo vuote poiché non ci sono titoli utilizzabili.
// Imposta la proprietà "CreateMissingOutlineLevels" su "false" per ignorare i livelli di contorno mancanti,
// e tratta le intestazioni di livello 5 come se fossero di livello 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Guarda anche

* class [OutlineOptions](../../outlineoptions/)
* class [PdfSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
