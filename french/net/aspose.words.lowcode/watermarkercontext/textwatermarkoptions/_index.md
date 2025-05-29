---
title: WatermarkerContext.TextWatermarkOptions
linktitle: TextWatermarkOptions
articleTitle: TextWatermarkOptions
second_title: Aspose.Words pour .NET
description: Découvrez des options personnalisables pour les filigranes d'image avec la propriété WatermarkerContext TextWatermarkOptions pour améliorer vos visuels et protéger votre contenu.
type: docs
weight: 50
url: /fr/net/aspose.words.lowcode/watermarkercontext/textwatermarkoptions/
---
## WatermarkerContext.TextWatermarkOptions property

Options pour le filigrane de l'image.

```csharp
public TextWatermarkOptions TextWatermarkOptions { get; }
```

## Exemples

Montre comment insérer du texte en filigrane dans le document à l'aide du contexte.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

WatermarkerContext watermarkerContext = new WatermarkerContext();
watermarkerContext.TextWatermark = watermarkText;

watermarkerContext.TextWatermarkOptions.Color = Color.Red;

Watermarker.Create(watermarkerContext)
    .From(doc)
    .To(ArtifactsDir + "LowCode.WatermarkContextText.docx")
    .Execute();
```

Montre comment insérer du texte en filigrane dans le document à partir du flux à l'aide du contexte.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    WatermarkerContext watermarkerContext = new WatermarkerContext();
    watermarkerContext.TextWatermark = watermarkText;

    watermarkerContext.TextWatermarkOptions.Color = Color.Red;

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkContextTextStream.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.Create(watermarkerContext)
            .From(streamIn)
            .To(streamOut, SaveFormat.Docx)
            .Execute();
}
```

### Voir également

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [WatermarkerContext](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
