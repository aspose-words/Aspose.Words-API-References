---
title: OutlineOptions.CreateMissingOutlineLevels
linktitle: CreateMissingOutlineLevels
articleTitle: CreateMissingOutlineLevels
second_title: Aspose.Words per .NET
description: Scopri come la proprietà CreateMissingOutlineLevels in OutlineOptions migliora le esportazioni di documenti generando automaticamente i livelli di struttura mancanti per una migliore organizzazione.
type: docs
weight: 30
url: /it/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

Ottiene o imposta un valore che determina se creare o meno livelli di struttura mancanti quando il documento viene esportato .

Il valore predefinito per questa proprietà è`falso`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

## Esempi

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

* class [OutlineOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
