---
title: GraphicsQualityOptions.TextRenderingHint
second_title: Référence de l'API Aspose.Words pour .NET
description: GraphicsQualityOptions propriété. Obtient ou définit le mode de rendu du texte associé à ce Graphics.
type: docs
weight: 70
url: /fr/net/aspose.words.saving/graphicsqualityoptions/textrenderinghint/
---
## GraphicsQualityOptions.TextRenderingHint property

Obtient ou définit le mode de rendu du texte associé à ce Graphics.

```csharp
public TextRenderingHint? TextRenderingHint { get; set; }
```

### Exemples

Montre comment définir les options de qualité de rendu lors de la conversion de documents en formats d'image.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions
{
    SmoothingMode = SmoothingMode.AntiAlias,
    TextRenderingHint = TextRenderingHint.ClearTypeGridFit,
    CompositingMode = CompositingMode.SourceOver,
    CompositingQuality = CompositingQuality.HighQuality,
    InterpolationMode = InterpolationMode.High,
    StringFormat = StringFormat.GenericTypographic
};

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
saveOptions.GraphicsQualityOptions = qualityOptions;

doc.Save(ArtifactsDir + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
```

### Voir également

* class [GraphicsQualityOptions](../)
* espace de noms [Aspose.Words.Saving](../../graphicsqualityoptions/)
* Assemblée [Aspose.Words](../../../)


