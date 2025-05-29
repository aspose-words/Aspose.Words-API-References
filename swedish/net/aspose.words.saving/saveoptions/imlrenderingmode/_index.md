---
title: SaveOptions.ImlRenderingMode
linktitle: ImlRenderingMode
articleTitle: ImlRenderingMode
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen SaveOptions ImlRenderingMode förbättrar InkML-objektrendering. Optimera din bläckrendering för bättre visuella resultat!
type: docs
weight: 90
url: /sv/net/aspose.words.saving/saveoptions/imlrenderingmode/
---
## SaveOptions.ImlRenderingMode property

Hämtar eller ställer in ett värde som avgör hur bläckobjekt (InkML) renderas.

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

// Om 'ImlRenderingMode.InkML' sätts ignoreras alternativ form för Ink-objektet (InkML) och renderas InkML självt.
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
