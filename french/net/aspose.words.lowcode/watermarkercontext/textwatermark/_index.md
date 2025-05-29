---
title: WatermarkerContext.TextWatermark
linktitle: TextWatermark
articleTitle: TextWatermark
second_title: Aspose.Words pour .NET
description: Découvrez la fonctionnalité WatermarkerContext TextWatermark pour ajouter facilement des filigranes de texte personnalisables, améliorant ainsi la sécurité et l'image de marque de votre contenu.
type: docs
weight: 40
url: /fr/net/aspose.words.lowcode/watermarkercontext/textwatermark/
---
## WatermarkerContext.TextWatermark property

Texte à utiliser comme filigrane.

```csharp
public string TextWatermark { get; set; }
```

## Remarques

Si les deux[`ImageWatermark`](../imagewatermark/) et`TextWatermark` sont spécifiés, le filigrane de texte remplace le filigrane d'image.

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

* class [WatermarkerContext](../)
* espace de noms [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* Assemblée [Aspose.Words](../../../)
