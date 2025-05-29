---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: Aspose.Words pour .NET
description: Découvrez comment la propriété ScaleImageToShapeSize de HtmlSaveOptions optimise la mise à l'échelle des images dans Aspose.Words pour les exportations HTML, MHTML ou EPUB. Améliorez vos documents !
type: docs
weight: 470
url: /fr/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Spécifie si les images sont mises à l'échelle par Aspose.Words à la taille de la forme englobante lors de l'exportation vers HTML, MHTML ou EPUB. La valeur par défaut est`vrai` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## Remarques

Dans un document Microsoft Word, une image est une forme. La forme a une taille, et l'image a sa propre taille. Les tailles ne sont pas directement liées. Par exemple, l'image peut mesurer 1024 x 786 pixels, , mais la forme qui l'affiche peut mesurer 400 x 300 points.

Pour afficher une image dans le navigateur, elle doit être mise à l'échelle à la taille de la forme. Le`ScaleImageToShapeSize` contrôle de propriété où la mise à l'échelle de l'image a lieu : dans Aspose.Words lors de l'exportation vers HTML ou dans le navigateur lors de l'affichage du document.

Quand`ScaleImageToShapeSize` est`vrai` , l'image est mise à l'échelle par Aspose.Words grâce à une mise à l'échelle de haute qualité lors de l'exportation au format HTML.`ScaleImageToShapeSize` est`FAUX`, l'image est sortie avec sa taille d'origine et le navigateur doit la mettre à l'échelle.

En général, les navigateurs effectuent une mise à l'échelle rapide et de mauvaise qualité. Par conséquent, vous obtiendrez généralement une meilleure qualité d'affichage dans le navigateur et une taille de fichier plus petite.`ScaleImageToShapeSize` est`vrai` , mais une meilleure qualité d'impression et une conversion plus rapide lorsque`ScaleImageToShapeSize` est`FAUX`.

Outre les formes contenant des images raster individuelles, cette option affecte également les formes de groupe constituées d'images raster. Si`ScaleImageToShapeSize` est`FAUX` et une forme de groupe contient des images raster dont la résolution intrinsèque est supérieure à la valeur spécifiée dans[`ImageResolution`](../imageresolution/)Aspose.Words augmentera la résolution de rendu de ce groupe. Cela permet de mieux préserver la qualité des images groupées haute résolution lors de l'enregistrement au format HTML.

## Exemples

Montre comment désactiver la mise à l'échelle des images selon leurs dimensions de forme parent lors de l'enregistrement au format .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insérez une forme qui contient une image, puis rendez cette forme considérablement plus petite que l'image.
Shape imageShape = builder.InsertImage(ImageDir + "Transparent background logo.png");
imageShape.Width = 50;
imageShape.Height = 50;

// L'enregistrement d'un document contenant des formes avec des images au format HTML créera un fichier image dans le système de fichiers local
// pour chaque forme. Le document HTML de sortie utilisera des balises <image> pour créer des liens vers ces images et les afficher.
// Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions pour déterminer
// s'il faut mettre à l'échelle toutes les images qui se trouvent à l'intérieur des formes aux tailles de leurs formes.
// Définir l'indicateur « ScaleImageToShapeSize » sur « true » réduira chaque image
// à la taille de la forme qui la contient, de sorte qu'aucune image enregistrée ne soit plus grande que ce que le document exige.
// Définir l'indicateur « ScaleImageToShapeSize » sur « false » préservera les tailles d'origine de ces images,
// qui prendra plus de place en échange de la préservation de la qualité de l'image.
HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);
```

### Voir également

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
