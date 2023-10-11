---
title: OutlineOptions.CreateMissingOutlineLevels
second_title: Aspose.Words per .NET API Reference
description: OutlineOptions proprietà. Ottiene o imposta un valore che determina se creare o meno livelli di struttura mancanti quando il documento viene esportato.
type: docs
weight: 30
url: /it/net/aspose.words.saving/outlineoptions/createmissingoutlinelevels/
---
## OutlineOptions.CreateMissingOutlineLevels property

Ottiene o imposta un valore che determina se creare o meno livelli di struttura mancanti quando il documento viene esportato.

Il valore predefinito per questa proprietà è`falso`.

```csharp
public bool CreateMissingOutlineLevels { get; set; }
```

### Esempi

Mostra come lavorare con i livelli di struttura che non contengono intestazioni corrispondenti quando si salva un documento PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci intestazioni che possono servire come voci di sommario dei livelli 1 e 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.1.1.1.1");
builder.Writeln("Heading 1.1.1.1.2");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Il documento PDF di output conterrà una struttura, ovvero un sommario che elenca le intestazioni nel corpo del documento.
// Facendo clic su una voce in questo schema ci porterà alla posizione della rispettiva intestazione.
// Imposta la proprietà "HeadingsOutlineLevels" su "5" per includere tutte le intestazioni dei livelli 5 e inferiori nella struttura.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 5;

// Questo documento contiene titoli di livello 1 e 5 e nessun titolo di livello 2, 3 e 4.
// Il documento PDF di output tratterà i livelli di struttura 2, 3 e 4 come "mancanti".
// Imposta la proprietà "CreateMissingOutlineLevels" su "true" per includere tutti i livelli mancanti nella struttura,
// lasciando le voci di contorno vuote poiché non ci sono intestazioni utilizzabili.
// Imposta la proprietà "CreateMissingOutlineLevels" su "false" per ignorare i livelli di struttura mancanti,
// e tratta i titoli di livello 5 della struttura come livello 2.
saveOptions.OutlineOptions.CreateMissingOutlineLevels = createMissingOutlineLevels;

doc.Save(ArtifactsDir + "PdfSaveOptions.CreateMissingOutlineLevels.pdf", saveOptions);
```

### Guarda anche

* class [OutlineOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../outlineoptions/)
* assemblea [Aspose.Words](../../../)


