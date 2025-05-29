---
title: TextEffect Enum
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words pour .NET
description: Découvrez l'énumération Aspose.Words.TextEffect pour des animations de texte dynamiques. Améliorez vos documents avec des effets attrayants pour une expérience utilisateur captivante.
type: docs
weight: 7270
url: /fr/net/aspose.words/texteffect/
---
## TextEffect enumeration

Effet d'animation pour les passages de texte.

```csharp
public enum TextEffect
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| None | `0` |  |
| LasVegasLights | `1` |  |
| BlinkingBackground | `2` |  |
| SparkleText | `3` |  |
| MarchingBlackAnts | `4` |  |
| MarchingRedAnts | `5` |  |
| Shimmer | `6` |  |

## Exemples

Montre comment appliquer un effet visuel à une course.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// Les anciennes versions de Microsoft Word ne prennent en charge que les effets d’animation de police.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### Voir également

* espace de noms [Aspose.Words](../../aspose.words/)
* Assemblée [Aspose.Words](../../)
