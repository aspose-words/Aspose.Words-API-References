---
title: LoadOptions.ConvertMetafilesToPng
linktitle: ConvertMetafilesToPng
articleTitle: ConvertMetafilesToPng
second_title: Aspose.Words für .NET
description: Konvertieren Sie WMF- und EMF-Metadateien mühelos in das PNG-Format mit LoadOptions. Vereinfachen Sie Ihre Bildverwaltung und verbessern Sie die Kompatibilität!
type: docs
weight: 30
url: /de/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Ruft ab oder legt fest, ob Metadateien konvertiert werden sollen (Wmf oderEmf ) Bilder zuPngBildformat.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

## Bemerkungen

Metadateien (Wmf oderEmf ) ist ein unkomprimiertes Bildformat und benötigt manchmal zu viel RAM, um Dokumente zu speichern und zu verarbeiten. Diese Option ermöglicht die Konvertierung aller Metadateibilder inPng beim Laden des Dokuments. Bitte beachten: Die Konvertierung von Vektorgrafiken in Raster verringert die Qualität der Bilder.

## Beispiele

Zeigt, wie WMF/EMF beim Laden des Dokuments in PNG konvertiert wird.

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

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
