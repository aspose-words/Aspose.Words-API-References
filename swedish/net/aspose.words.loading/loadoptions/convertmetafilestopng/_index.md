---
title: LoadOptions.ConvertMetafilesToPng
linktitle: ConvertMetafilesToPng
articleTitle: ConvertMetafilesToPng
second_title: Aspose.Words för .NET
description: Konvertera enkelt WMF- och EMF-metafiler till PNG-format med LoadOptions. Förenkla din bildhantering och förbättra kompatibiliteten idag!
type: docs
weight: 30
url: /sv/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Hämtar eller anger om metafil ska konverteras(Wmf ellerEmf ) bilder tillPngbildformat.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

## Anmärkningar

Metafiler (Wmf ellerEmf ) är ett okomprimerat bildformat och kräver ibland för mycket RAM för att lagra och bearbeta dokument. Det här alternativet gör det möjligt att konvertera alla metafilbilder tillPng vid laddning av dokument. Observera - konvertering av vektorgrafik till raster minskar bildernas kvalitet.

## Exempel

Visar hur man konverterar WMF/EMF till PNG när dokumentet laddas.

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

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
