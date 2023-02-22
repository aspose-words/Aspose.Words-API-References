---
title: Font.HasDmlEffect
second_title: Référence de l'API Aspose.Words pour .NET
description: Font méthode. Vérifie si un effet de texte particulier de DrawingML est appliqué.
type: docs
weight: 560
url: /fr/net/aspose.words/font/hasdmleffect/
---
## Font.HasDmlEffect method

Vérifie si un effet de texte particulier de DrawingML est appliqué.

```csharp
public bool HasDmlEffect(TextDmlEffect dmlEffectType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dmlEffectType | TextDmlEffect | Type d'effet de texte DrawingML. |

### Return_Value

True si un effet de texte DrawingML particulier est appliqué.

### Exemples

Montre comment vérifier si une exécution affiche un effet de texte DrawingML.

```csharp
Document doc = new Document(MyDir + "DrawingML text effects.docx");

RunCollection runs = doc.FirstSection.Body.FirstParagraph.Runs;

Assert.True(runs[0].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[1].Font.HasDmlEffect(TextDmlEffect.Shadow));
Assert.True(runs[2].Font.HasDmlEffect(TextDmlEffect.Reflection));
Assert.True(runs[3].Font.HasDmlEffect(TextDmlEffect.Effect3D));
Assert.True(runs[4].Font.HasDmlEffect(TextDmlEffect.Fill));
```

### Voir également

* enum [TextDmlEffect](../../textdmleffect/)
* class [Font](../)
* espace de noms [Aspose.Words](../../font/)
* Assemblée [Aspose.Words](../../../)


