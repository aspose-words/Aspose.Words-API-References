---
title: Font.HasDmlEffect
linktitle: HasDmlEffect
articleTitle: HasDmlEffect
second_title: Aspose.Words pour .NET
description: Découvrez si un effet de texte DrawingML spécifique est appliqué avec la méthode Font HasDmlEffect. Améliorez l'attrait visuel de votre document sans effort !
type: docs
weight: 570
url: /fr/net/aspose.words/font/hasdmleffect/
---
## Font.HasDmlEffect method

Vérifie si un effet de texte DrawingML particulier est appliqué.

```csharp
public bool HasDmlEffect(TextDmlEffect dmlEffectType)
```

| Paramètre | Taper | La description |
| --- | --- | --- |
| dmlEffectType | TextDmlEffect | Type d'effet de texte DrawingML. |

### Return_Value

`vrai` si un effet de texte DrawingML particulier est appliqué.

## Exemples

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
* espace de noms [Aspose.Words](../../../aspose.words/)
* Assemblée [Aspose.Words](../../../)
