---
title: LoadOptions.ConvertMetafilesToPng
linktitle: ConvertMetafilesToPng
articleTitle: ConvertMetafilesToPng
second_title: Aspose.Words för .NET
description: LoadOptions ConvertMetafilesToPng fast egendom. Hämtar eller ställer in om metafil ska konverteras Wmf ellerEmf  bilder tillPng bildformat i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.loading/loadoptions/convertmetafilestopng/
---
## LoadOptions.ConvertMetafilesToPng property

Hämtar eller ställer in om metafil ska konverteras (Wmf ellerEmf ) bilder tillPng bildformat.

```csharp
public bool ConvertMetafilesToPng { get; set; }
```

## Anmärkningar

Metafiler (Wmf ellerEmf ) är ett okomprimerat bildformat och kräver ibland för mycket RAM-minne för att hålla och bearbeta dokument. Detta alternativ gör det möjligt att konvertera alla metafilbilder tillPng vid dokumentladdning. Observera - konvertering av vektorgrafik till raster minskar kvaliteten på bilderna.

## Exempel

Visar hur man konverterar WMF/EMF till PNG under laddning av dokument.

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

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
