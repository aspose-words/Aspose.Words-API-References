---
title: SaveOptions.ImlRenderingMode
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words för .NET
description: SaveOptions ImlRenderingMode fast egendom. Hämtar eller ställer in ett värde som bestämmer hur bläckobjekt InkML renderas i C#.
type: docs
weight: 90
url: /sv/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Hämtar eller ställer in ett värde som bestämmer hur bläckobjekt (InkML) renderas.

```csharp
public ImlRenderingMode ImlRenderingMode { get; set; }
```

## Anmärkningar

Standardvärdet ärInkML .

Den här egenskapen används när dokumentet exporteras till fasta sidformat.

## Exempel

Visar hur man renderar Ink-objekt.

```csharp
Document doc = new Document(MyDir + "Ink object.docx");

// Set 'ImlRenderingMode.InkML' ignorerar fall-back form av ink (InkML) objekt och renderar InkML själv.
// Om renderingsresultatet är otillfredsställande,
// använd 'ImlRenderingMode.Fallback' för att få ett resultat som liknar tidigare versioner.
ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg)
{
    ImlRenderingMode = ImlRenderingMode.InkML
};

doc.Save(ArtifactsDir + "ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

### Se även

* enum [ImlRenderingMode](../../imlrenderingmode/)
* class [SaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
