---
title: OutlineOptions.ExpandedOutlineLevels
linktitle: ExpandedOutlineLevels
articleTitle: ExpandedOutlineLevels
second_title: Aspose.Words per .NET
description: Scopri la proprietà ExpandedOutlineLevels in OutlineOptions, che ti consente di personalizzare la visibilità della struttura del documento per una navigazione e un'esperienza utente migliorate.
type: docs
weight: 60
url: /it/net/aspose.words.saving/outlineoptions/expandedoutlinelevels/
---
## OutlineOptions.ExpandedOutlineLevels property

Specifica quanti livelli nel documento devono essere visualizzati espansi quando il file viene visualizzato.

```csharp
public int ExpandedOutlineLevels { get; set; }
```

## Osservazioni

Tieni presente che questa opzione non funzionerà se si salva in formato XPS.

Specificando 0 la struttura del documento verrà compressa; specificando 1, il primo livello items nella struttura verrà espanso e così via.

Il valore predefinito è 0. L'intervallo valido è compreso tra 0 e 9.

## Esempi

Mostra come convertire un intero documento in PDF con tre livelli nella struttura del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire le intestazioni dei livelli da 1 a 5.
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

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Il documento PDF di output conterrà una struttura, ovvero un indice che elenca le intestazioni nel corpo del documento.
// Cliccando su una voce in questo schema verremo indirizzati alla posizione della rispettiva intestazione.
// Impostare la proprietà "HeadingsOutlineLevels" su "4" per escludere dalla struttura tutte le intestazioni i cui livelli sono superiori a 4.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Se una voce di struttura ha voci successive di livello superiore tra sé stessa e la voce successiva dello stesso livello o di livello inferiore,
// apparirà una freccia a sinistra della voce. Questa voce è la "proprietaria" di diverse "sotto-voci" di questo tipo.
// Nel nostro documento, le voci di struttura del 5° livello di intestazione sono sottovoci della seconda voce di struttura del 4° livello,
// le voci di 4° e 5° livello di intestazione sono sottovoci della seconda voce di 3° livello, e così via.
// Nella struttura, possiamo cliccare sulla freccia della voce "proprietario" per comprimere/espandere tutte le sue sotto-voci.
// Imposta la proprietà "ExpandedOutlineLevels" su "2" per espandere automaticamente tutte le voci di struttura di livello 2 e inferiore dell'intestazione
// e comprimere tutte le voci di livello 3 e superiori quando apriamo il documento.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Guarda anche

* class [OutlineOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
