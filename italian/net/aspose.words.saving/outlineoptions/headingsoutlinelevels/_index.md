---
title: OutlineOptions.HeadingsOutlineLevels
second_title: Aspose.Words per .NET API Reference
description: OutlineOptions proprietà. Specifica quanti livelli di intestazioni paragrafi formattati con gli stili di intestazione includere nella struttura del documento .
type: docs
weight: 70
url: /it/net/aspose.words.saving/outlineoptions/headingsoutlinelevels/
---
## OutlineOptions.HeadingsOutlineLevels property

Specifica quanti livelli di intestazioni (paragrafi formattati con gli stili di intestazione) includere nella struttura del documento .

```csharp
public int HeadingsOutlineLevels { get; set; }
```

### Osservazioni

Specificare 0 per nessuna intestazione nella struttura; specificare 1 per un livello di intestazioni nella struttura e così via.

Il valore predefinito è 0. L'intervallo valido è compreso tra 0 e 9.

### Esempi

Mostra come convertire un intero documento in PDF con tre livelli nella struttura del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce le intestazioni dei livelli da 1 a 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Crea un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui il metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Il documento PDF di output conterrà una struttura, ovvero un sommario che elenca le intestazioni nel corpo del documento.
// Facendo clic su una voce in questo schema ci porterà alla posizione della rispettiva intestazione.
// Imposta la proprietà "HeadingsOutlineLevels" su "4" per escludere dalla struttura tutte le intestazioni i cui livelli sono superiori a 4.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Se una voce di struttura ha voci successive di livello superiore tra sé e la voce successiva dello stesso livello o di livello inferiore,
// apparirà una freccia a sinistra della voce. Questa voce è il "proprietario" di diverse "sottovoci" di questo tipo.
// Nel nostro documento, le voci di struttura del 5° livello di intestazione sono sottovoci della seconda voce di struttura di 4° livello,
// le voci di 4° e 5° livello di intestazione sono sottovoci della seconda voce di 3° livello e così via.
// Nella struttura, possiamo fare clic sulla freccia della voce "proprietario" per comprimere/espandere tutte le sue sottovoci.
// Imposta la proprietà "ExpandedOutlineLevels" su "2" per espandere automaticamente tutte le voci di intestazione di livello 2 e di struttura inferiore
// e comprime tutte le voci di livello 3 e superiori quando apriamo il documento.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Guarda anche

* class [OutlineOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../outlineoptions/)
* assemblea [Aspose.Words](../../../)


