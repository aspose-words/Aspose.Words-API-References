---
title: Dml3DEffectsRenderingMode Enum
linktitle: Dml3DEffectsRenderingMode
articleTitle: Dml3DEffectsRenderingMode
second_title: Aspose.Words pour .NET
description: Découvrez comment améliorer vos documents avec l'énumération Dml3DEffectsRenderingMode d'Aspose.Words pour un rendu de forme 3D supérieur et un impact visuel.
type: docs
weight: 5650
url: /fr/net/aspose.words.saving/dml3deffectsrenderingmode/
---
## Dml3DEffectsRenderingMode enumeration

Spécifie comment les effets de forme 3D sont rendus.

```csharp
public enum Dml3DEffectsRenderingMode
```

### Valeurs

| Nom | Évaluer | La description |
| --- | --- | --- |
| Basic | `0` | Un rendu léger et stable, basé sur le moteur interne, mais les effets avancés tels que l'éclairage, les matériaux et d'autres effets supplémentaires ne sont pas affichés lors de l'utilisation de ce mode. Veuillez consulter la documentation pour plus de détails. |
| Advanced | `1` | Rendu d'une liste étendue d'effets spéciaux, y compris des effets 3D avancés tels que les biseaux, l'éclairage et les matériaux. |

## Exemples

Montre comment les effets 3D sont rendus.

```csharp
Document doc = new Document(MyDir + "DrawingML shape 3D effects.docx");

RenderCallback warningCallback = new RenderCallback();
doc.WarningCallback = warningCallback;

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.Dml3DEffectsRenderingMode = Dml3DEffectsRenderingMode.Advanced;

doc.Save(ArtifactsDir + "PdfSaveOptions.Dml3DEffectsRenderingModeTest.pdf", saveOptions);
```

### Voir également

* espace de noms [Aspose.Words.Saving](../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../)
