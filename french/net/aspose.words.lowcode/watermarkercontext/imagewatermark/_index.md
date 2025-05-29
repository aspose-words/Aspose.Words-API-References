---
title: WatermarkerContext.ImageWatermark
linktitle: ImageWatermark
articleTitle: ImageWatermark
second_title: Aspose.Words pour .NET
description: Découvrez comment améliorer vos images avec la propriété WatermarkerContext ImageWatermark, vous permettant d'ajouter des images de filigrane personnalisées sans effort.
type: docs
weight: 20
url: /fr/net/aspose.words.lowcode/watermarkercontext/imagewatermark/
---
## WatermarkerContext.ImageWatermark property

Octets d'image à utiliser comme filigrane.

```csharp
public byte[] ImageWatermark { get; set; }
```

## Remarques

Si les deux`ImageWatermark` et[`TextWatermark`](../textwatermark/) sont spécifiés, le filigrane de texte remplace le filigrane d'image.

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

* class [WatermarkerContext](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
