---
title: ImageSaveOptions.Clone
linktitle: Clone
articleTitle: Clone
second_title: Aspose.Words per .NET
description: Scopri il metodo ImageSaveOptions Clone per creare senza sforzo un clone profondo dei tuoi oggetti, migliorando l'efficienza e la flessibilità della tua codifica.
type: docs
weight: 210
url: /it/net/aspose.words.saving/imagesaveoptions/clone/
---
## ImageSaveOptions.Clone method

Crea un clone profondo di questo oggetto.

```csharp
public ImageSaveOptions Clone()
```

## Esempi

Mostra come selezionare una velocità bit per pixel con cui trasformare un documento in un'immagine.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.InsertImage(ImageDir + "Logo.jpg");

// Quando salviamo il documento come immagine, possiamo passare un oggetto SaveOptions a
// seleziona un formato pixel per l'immagine che verrà generata dall'operazione di salvataggio.
// Diverse velocità di bit per pixel influiranno sulla qualità e sulle dimensioni del file dell'immagine generata.
ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PixelFormat = imagePixelFormat;

// Possiamo clonare le istanze di ImageSaveOptions.
Assert.AreNotEqual(imageSaveOptions, imageSaveOptions.Clone());

doc.Save(ArtifactsDir + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
```

### Guarda anche

* class [ImageSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
