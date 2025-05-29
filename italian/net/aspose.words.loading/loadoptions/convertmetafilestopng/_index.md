---
title: LoadOptions.ConvertMetafilesToPng
linktitle: ConvertMetafilesToPng
articleTitle: ConvertMetafilesToPng
second_title: Aspose.Words per .NET
description: Converti facilmente i metafile WMF ed EMF in formato PNG con LoadOptions. Semplifica la gestione delle immagini e migliora la compatibilità oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Ottiene o imposta se convertire metafile(Wmf OEmf ) immagini aPngformato immagine.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

## Osservazioni

Metafile (Wmf OEmf ) è un formato di immagine non compresso e talvolta richiede troppa RAM per contenere ed elaborare il documento. Questa opzione consente di convertire tutte le immagini metafile inPng durante il caricamento del documento. Nota: la conversione della grafica vettoriale in raster riduce la qualità delle immagini.

## Esempi

Mostra come convertire WMF/EMF in PNG durante il caricamento del documento.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Image);
shape.ImageData.SetImage(ImageDir + "Windows MetaFile.wmf");
shape.Width = 100;
shape.Height = 100;

doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

doc.Save(ArtifactsDir + "Image.CreateImageDirectly.docx");

shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

TestUtil.VerifyImageInShape(1600, 1600, ImageType.Wmf, shape);

LoadOptions loadOptions = new LoadOptions();
loadOptions.ConvertMetafilesToPng = true;

doc = new Document(ArtifactsDir + "Image.CreateImageDirectly.docx", loadOptions);
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
```

### Guarda anche

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
