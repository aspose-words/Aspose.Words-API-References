---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize method"
linktitle: "get_ScaleImageToShapeSize"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize méthode. Spécifie si les images sont redimensionnées par Aspose.Words à la taille de la forme de délimitation lors de l'exportation vers HTML, MHTML ou EPUB. La valeur par défaut est true en C++."
type: docs
weight: 46000
url: /fr/cpp/aspose.words.saving/htmlsaveoptions/get_scaleimagetoshapesize/
---
## HtmlSaveOptions::get_ScaleImageToShapeSize method


Spécifie si les images sont redimensionnées par Aspose.Words à la taille de la forme englobante lors de l'exportation vers HTML, MHTML ou EPUB. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ScaleImageToShapeSize() const
```

## Remarques


Une image dans un document Microsoft Word est une forme. La forme possède une taille et l'image a sa propre taille. Les tailles ne sont pas directement liées. Par exemple, l'image peut mesurer 1024 x 786 pixels, mais la forme qui affiche cette image peut mesurer 400 x 300 points.

Afin d'afficher une image dans le navigateur, elle doit être redimensionnée à la taille de la forme. La propriété [ScaleImageToShapeSize](./) contrôle l'endroit où le redimensionnement de l'image a lieu : dans Aspose.Words lors de l'exportation vers HTML ou dans le navigateur lors de l'affichage du document.

Lorsque [ScaleImageToShapeSize](./) est **true**, l'image est redimensionnée par [Aspose.Words](../../../aspose.words/) en utilisant un redimensionnement de haute qualité lors de l'exportation vers HTML. Lorsque [ScaleImageToShapeSize](./) est **false**, l'image est exportée avec sa taille d'origine et le navigateur doit la redimensionner.

En général, les navigateurs effectuent un redimensionnement rapide et de mauvaise qualité. En conséquence, vous obtiendrez normalement une meilleure qualité d'affichage dans le navigateur et une taille de fichier plus petite lorsque [ScaleImageToShapeSize](./) est **true**, mais une meilleure qualité d'impression et une conversion plus rapide lorsque [ScaleImageToShapeSize](./) est **false**.

En plus des formes contenant des images raster individuelles, cette option affecte également les formes groupées composées d'images raster. Si [ScaleImageToShapeSize](./) est **false** et qu'une forme groupée contient des images raster dont la résolution intrinsèque est supérieure à la valeur spécifiée dans [ImageResolution](../get_imageresolution/), Aspose.Words augmentera la résolution de rendu pour ce groupe. Cela permet de mieux préserver la qualité des images haute résolution groupées lors de l'enregistrement au format HTML.

## Voir aussi

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
