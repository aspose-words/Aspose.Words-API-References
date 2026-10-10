---
title: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape méthode"
linktitle: "get_Shape"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape méthode. Spécifie la forme que le moteur de publipostage doit insérer dans le document en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.mailmerging/imagefieldmergingargs/get_shape/
---
## ImageFieldMergingArgs::get_Shape method


Spécifie la forme que le moteur de publipostage doit insérer dans le document.

```cpp
const System::SharedPtr<Aspose::Words::Drawing::Shape> & Aspose::Words::MailMerging::ImageFieldMergingArgs::get_Shape() const
```

## Remarques


Lorsque cette propriété est spécifiée, le moteur de publipostage ignore toutes les autres propriétés comme [ImageFileName](../get_imagefilename/) ou [ImageStream](../get_imagestream/) et insère simplement la forme dans le document.

Utilisez cette propriété pour contrôler complètement le processus de fusion d'un champ de fusion d'image. Par exemple, vous pouvez spécifier [WrapType](../../../aspose.words.drawing/shapebase/get_wraptype/) ou toute autre propriété de forme afin d'ajuster finement le nœud résultant. Cependant, veuillez noter que vous êtes responsable de fournir le contenu de la forme.
## Voir aussi

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [ImageFieldMergingArgs](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
