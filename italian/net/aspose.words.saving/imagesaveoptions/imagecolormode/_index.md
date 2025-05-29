---
title: ImageSaveOptions.ImageColorMode
linktitle: ImageColorMode
articleTitle: ImageColorMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà ImageColorMode di ImageSaveOptions per personalizzare e ottimizzare facilmente la modalità colore delle immagini generate. Migliora le tue immagini oggi stesso!
type: docs
weight: 50
url: /it/net/aspose.words.saving/imagesaveoptions/imagecolormode/
---
## ImageSaveOptions.ImageColorMode property

Ottiene o imposta la modalità colore per le immagini generate.

```csharp
public ImageColorMode ImageColorMode { get; set; }
```

## Osservazioni

Questa proprietà ha effetto solo quando si salva in formati di immagini raster.

Il valore predefinito èNone.

## Esempi

Mostra come impostare una modalità colore durante il rendering dei documenti.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// seleziona una modalità colore per l'immagine che verrà generata dall'operazione di salvataggio.
// Se impostiamo la proprietà "ImageColorMode" su "ImageColorMode.BlackAndWhite",
// l'operazione di salvataggio applicherà una riduzione del colore in scala di grigi durante il rendering del documento.
 // Se impostiamo la proprietà "ImageColorMode" su "ImageColorMode.Grayscale",
// l'operazione di salvataggio trasformerà il documento in un'immagine monocromatica.
// Se impostiamo la proprietà "ImageColorMode" su "None", l'operazione di salvataggio applicherà il metodo predefinito
// e conserva tutti i colori del documento nell'immagine di output.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.ImageColorMode = imageColorMode;

doc.Save(ArtifactsDir + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

### Guarda anche

* enum [ImageColorMode](../../imagecolormode/)
* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
