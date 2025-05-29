---
title: ParagraphFormat.IsHeading
linktitle: IsHeading
articleTitle: IsHeading
second_title: Aspose.Words per .NET
description: Scopri come la proprietà IsHeading migliora la formattazione del tuo documento identificando gli stili di intestazione incorporati per una migliore organizzazione e chiarezza.
type: docs
weight: 140
url: /it/net/aspose.words/paragraphformat/isheading/
---
## ParagraphFormat.IsHeading property

Vero quando lo stile del paragrafo è uno degli stili di intestazione incorporati.

```csharp
public bool IsHeading { get; }
```

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

### Guarda anche

* class [ParagraphFormat](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
