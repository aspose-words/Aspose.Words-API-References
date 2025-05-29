---
title: PageSetup.PageHeight
linktitle: PageHeight
articleTitle: PageHeight
second_title: Aspose.Words per .NET
description: Scopri la proprietà PageHeight di PageSetup per gestire in modo efficiente l'altezza del tuo documento in punti, migliorandone il layout e la presentazione.
type: docs
weight: 310
url: /it/net/aspose.words/pagesetup/pageheight/
---
## PageSetup.PageHeight property

Restituisce o imposta l'altezza della pagina in punti.

```csharp
public double PageHeight { get; set; }
```

## Esempi

Mostra come inserire un'immagine e utilizzarla come filigrana.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci l'immagine nell'intestazione in modo che sia visibile su ogni pagina.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Posiziona l'immagine al centro della pagina.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### Guarda anche

* class [PageSetup](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
