---
title: Font.Shading
second_title: Référence de l'API Aspose.Words pour .NET
description: Font propriété. Renvoie un objet Shading qui fait référence à la mise en forme de lombrage de la police.
type: docs
weight: 320
url: /fr/net/aspose.words/font/shading/
---
## Font.Shading property

Renvoie un objet Shading qui fait référence à la mise en forme de l'ombrage de la police.

```csharp
public Shading Shading { get; }
```

### Exemples

Montre comment appliquer un ombrage au texte créé par un générateur de document.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// Une façon de rendre visible le texte créé à l'aide de notre couleur de police blanche
// est d'appliquer un effet d'ombrage de fond.
Shading shading = builder.Font.Shading;
shading.Texture = TextureIndex.TextureDiagonalUp;
shading.BackgroundPatternColor = Color.OrangeRed;
shading.ForegroundPatternColor = Color.DarkBlue;

builder.Writeln("White text on an orange background with a two-tone texture.");

doc.Save(ArtifactsDir + "Font.Shading.docx");
```

### Voir également

* class [Shading](../../shading/)
* class [Font](../)
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)


