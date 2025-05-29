---
title: Font.Shading
linktitle: Shading
articleTitle: Shading
second_title: Aspose.Words pour .NET
description: Découvrez la propriété Font Shading, qui fournit un objet Shading pour une mise en forme de police personnalisable, améliorant ainsi l'attrait visuel de votre texte.
type: docs
weight: 330
url: /fr/net/aspose.words/font/shading/
---
## Font.Shading property

Renvoie un[`Shading`](../../shading/) objet qui fait référence au formatage d'ombrage de la police.

```csharp
public Shading Shading { get; }
```

## Exemples

Montre comment appliquer un ombrage au texte créé par un générateur de documents.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Color = Color.White;

// Une façon de rendre visible le texte créé à l'aide de notre couleur de police blanche
// consiste à appliquer un effet d'ombrage d'arrière-plan.
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
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
