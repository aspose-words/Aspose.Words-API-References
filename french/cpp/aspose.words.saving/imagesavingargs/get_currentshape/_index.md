---
title: "Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape méthode"
linktitle: "get_CurrentShape"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape méthode. Obtient l’objet ShapeBase correspondant à la forme ou au groupe de formes qui est sur le point d’être enregistré en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.saving/imagesavingargs/get_currentshape/
---
## ImageSavingArgs::get_CurrentShape method


Obtient l’objet [ShapeBase](../../../aspose.words.drawing/shapebase/) correspondant à la forme ou au groupe de formes qui est sur le point d’être enregistré.

```cpp
System::SharedPtr<Aspose::Words::Drawing::ShapeBase> Aspose::Words::Saving::ImageSavingArgs::get_CurrentShape() const
```

## Remarques


[IImageSavingCallback](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [ShapeBase](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing [ShapeType](../../../aspose.words.drawing/shapebase/get_shapetype/) with [Group](../../../aspose.words.drawing/shapetype/) or by casting it to one of derived classes: [Shape](../../../aspose.words.drawing/shape/) or [GroupShape](../../../aspose.words.drawing/groupshape/).

Aspose.Words utilise le nom de fichier du document et un numéro unique pour générer un nom de fichier unique pour chaque image trouvée dans le document. Vous pouvez utiliser la propriété [CurrentShape](./) pour générer un nom de fichier « meilleur » en examinant les propriétés de la forme telles que [Title](../../../aspose.words.drawing/imagedata/get_title/) (forme uniquement), [SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) (forme uniquement) et [Name](../../../aspose.words.drawing/shapebase/get_name/). Bien sûr, vous pouvez créer des noms de fichiers en utilisant d’autres propriétés ou critères, mais notez que les noms de fichiers secondaires doivent être uniques au cours de l’opération d’exportation.

Certaines images du document peuvent être indisponibles. Pour vérifier la disponibilité d’une image, utilisez la propriété [IsImageAvailable](../get_isimageavailable/).
## Voir aussi

* Class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* Class [ImageSavingArgs](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
