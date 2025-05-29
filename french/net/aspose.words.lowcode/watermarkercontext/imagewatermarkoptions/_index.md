---
title: WatermarkerContext.ImageWatermarkOptions
linktitle: ImageWatermarkOptions
articleTitle: ImageWatermarkOptions
second_title: Aspose.Words pour .NET
description: Découvrez des options de filigrane de texte personnalisables avec WatermarkerContext pour améliorer vos images et protéger efficacement l'identité de votre marque.
type: docs
weight: 30
url: /fr/net/aspose.words.lowcode/watermarkercontext/imagewatermarkoptions/
---
## WatermarkerContext.ImageWatermarkOptions property

Options pour le filigrane de texte.

```csharp
public ImageWatermarkOptions ImageWatermarkOptions { get; }
```

## Exemples

Montre comment insérer une image de filigrane dans le document à l'aide du contexte.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

watermarkerContext.ImageWatermarkOptions.Scale = 50;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextImage.docx")
    .Execute();
```

Montre comment insérer une image de filigrane dans le document à partir d'un flux à l'aide du contexte.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.ImageWatermark = File.ReadAllBytes(watermarkImage);

    watermarkerContext.ImageWatermarkOptions.Scale = 50;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextImageStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Voir également

* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [WatermarkerContext](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
