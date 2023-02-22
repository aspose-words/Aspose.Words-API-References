---
title: LoadOptions.ConvertMetafilesToPng
second_title: Aspose.Words per .NET API Reference
description: LoadOptions proprietà. Ottiene o imposta se convertire il metafile Wmf oEmf  immagini aPng formato immagine.
type: docs
weight: 30
url: /it/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Ottiene o imposta se convertire il metafile (Wmf oEmf ) immagini aPng formato immagine.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

### Osservazioni

Metafile (Wmf oEmf ) è un formato di immagine non compresso e talvolta richiede molta RAM per contenere ed elaborare il documento. Questa opzione consente di convertire tutte le immagini del metafile inPng durante il caricamento del documento. Nota: la conversione della grafica vettoriale in raster riduce la qualità delle immagini.

### Esempi

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

#if NET48
            TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
#elif NET5_0_OR_GREATER
            TestUtil.VerifyImageInShape(1666, 1666, ImageType.Png, shape);
#endif
```

### Guarda anche

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../loadoptions/)
* assemblea [Aspose.Words](../../../)


