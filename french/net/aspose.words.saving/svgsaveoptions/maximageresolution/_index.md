---
title: SvgSaveOptions.MaxImageResolution
linktitle: MaxImageResolution
articleTitle: MaxImageResolution
second_title: Aspose.Words pour .NET
description: Contrôlez la qualité de vos images raster exportées avec SvgSaveOptions MaxImageResolution. Définissez la densité de pixels pour des résultats optimaux. Valeur par défaut : 0.
type: docs
weight: 50
url: /fr/net/aspose.words.saving/svgsaveoptions/maximageresolution/
---
## SvgSaveOptions.MaxImageResolution property

Récupère ou définit une valeur en pixels par pouce qui limite la résolution des images raster exportées. La valeur par défaut est zéro.

```csharp
public int MaxImageResolution { get; set; }
```

## Remarques

Si la valeur de cette propriété est différente de zéro, elle limite la résolution des images raster exportées. Autrement dit, les images à haute résolution sont rééchantillonnées jusqu'à la limite et les images à basse résolution sont exportées telles quelles.

Si la valeur de cette propriété est zéro, toutes les images raster sont exportées sans rééchantillonnage.

## Exemples

Montre comment définir une limite pour la résolution de l'image.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

### Voir également

* class [SvgSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
