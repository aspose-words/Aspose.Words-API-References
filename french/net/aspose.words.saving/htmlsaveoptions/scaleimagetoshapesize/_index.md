---
title: HtmlSaveOptions.ScaleImageToShapeSize
linktitle: ScaleImageToShapeSize
articleTitle: ScaleImageToShapeSize
second_title: Aspose.Words pour .NET
description: HtmlSaveOptions ScaleImageToShapeSize propriété. Spécifie si les images sont mises à léchelle par Aspose.Words à la taille de la forme englobante lors de lexportation au format HTML MHTML ou EPUB. La valeur par défaut estvrai  en C#.
type: docs
weight: 450
url: /fr/net/aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/
---
## HtmlSaveOptions.ScaleImageToShapeSize property

Spécifie si les images sont mises à l'échelle par Aspose.Words à la taille de la forme englobante lors de l'exportation au format HTML, MHTML ou EPUB. La valeur par défaut est`vrai` .

```csharp
public bool ScaleImageToShapeSize { get; set; }
```

## Remarques

Une image dans un document Microsoft Word est une forme. La forme a une taille et image a sa propre taille. Les tailles ne sont pas directement liées. Par exemple, l'image peut faire 1024 x 786 pixels, mais la forme qui affiche cette image peut faire 400 x 300 points.

Afin d'afficher une image dans le navigateur, elle doit être adaptée à la taille de la forme. Le`ScaleImageToShapeSize` La propriété contrôle où la mise à l'échelle de l'image a lieu : dans Aspose.Words lors de l'exportation au format HTML ou dans le navigateur lors de l'affichage du document.

Quand`ScaleImageToShapeSize` est`vrai` , l'image est mise à l'échelle par Aspose.Words en utilisant une mise à l'échelle de haute qualité lors de l'exportation au format HTML. Quand`ScaleImageToShapeSize` est`FAUX`, l'image est affichée avec sa taille d'origine et le navigateur doit la mettre à l'échelle.

En général, les navigateurs effectuent une mise à l'échelle rapide et de mauvaise qualité. En conséquence, vous obtiendrez normalement une meilleure qualité d'affichage dans le navigateur et une taille de fichier plus petite lorsque`ScaleImageToShapeSize` est`vrai` , mais meilleure qualité d'impression et conversion plus rapide lorsque`ScaleImageToShapeSize` est`FAUX`.

En plus des formes contenant des images raster individuelles, cette option affecte également les formes de groupe consistant d'images raster. Si`ScaleImageToShapeSize` est`FAUX` et une forme de groupe contient des images raster dont la résolution intrinsèque est supérieure à la valeur spécifiée dans[`ImageResolution`](../imageresolution/), Aspose.Words will augmentera la résolution de rendu pour ce groupe. Cela permet de mieux préserver la qualité des images groupées haute résolution lors de l'enregistrement au format HTML.

## Exemples

Montre comment désactiver la mise à l’échelle des images selon les dimensions de leur forme parent lors de l’enregistrement au format .html.

```csharp
Document doc = new Document();
            DocumentBuilder builder = new DocumentBuilder(doc);

            // Insère une forme qui contient une image, puis rend cette forme considérablement plus petite que l'image.
#if NET48 || JAVA
            Image image = Image.FromFile(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Size.Width);
            Assert.AreEqual(400, image.Size.Height);
#elif NET5_0_OR_GREATER
            SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png");

            Assert.AreEqual(400, image.Width);
            Assert.AreEqual(400, image.Height);
#endif

            Shape imageShape = builder.InsertImage(image);
            imageShape.Width = 50;
            imageShape.Height = 50;

            // L'enregistrement d'un document contenant des formes avec des images au format HTML créera un fichier image dans le système de fichiers local
            // pour chacune de ces formes. Le document HTML de sortie utilisera <image> balises pour créer un lien vers et afficher ces images.
            // Lorsque nous enregistrons le document au format HTML, nous pouvons passer un objet SaveOptions pour déterminer
            // s'il faut mettre à l'échelle toutes les images qui se trouvent à l'intérieur des formes selon la taille de leurs formes.
            // Définir l'indicateur "ScaleImageToShapeSize" sur "true" réduira chaque image
            // à la taille de la forme qui la contient, afin qu'aucune image enregistrée ne soit plus grande que ce que le document exige.
            // Définir le flag "ScaleImageToShapeSize" sur "false" conservera les tailles d'origine de ces images,
            // qui prendra plus de place en échange de la préservation de la qualité de l'image.
            HtmlSaveOptions options = new HtmlSaveOptions { ScaleImageToShapeSize = scaleImageToShapeSize };

            doc.Save(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.html", options);

            FileInfo fileInfo = new FileInfo(ArtifactsDir + "HtmlSaveOptions.ScaleImageToShapeSize.001.png");

#if NET48 || JAVA
        if (scaleImageToShapeSize)
            Assert.That(3000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(20000, Is.LessThan(fileInfo.Length));
#elif NET5_0_OR_GREATER
        if (scaleImageToShapeSize)
            Assert.That(10000, Is.AtLeast(fileInfo.Length));
        else
            Assert.That(30000, Is.LessThan(fileInfo.Length));
#endif
```

### Voir également

* property [ImageResolution](../imageresolution/)
* class [HtmlSaveOptions](../)
* espace de noms [Aspose.Words.Saving](../../../aspose.words.saving/)
* Assemblée [Aspose.Words](../../../)
