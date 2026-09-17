---
title: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet méthode"
linktitle: "get_SavePictureBullet"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet méthode. Lorsque false, les données PictureBullet ne sont pas enregistrées dans le document de sortie. La valeur par défaut est true en C++."
type: docs
weight: 6000
url: /fr/cpp/aspose.words.saving/docsaveoptions/get_savepicturebullet/
---
## DocSaveOptions::get_SavePictureBullet method


Lorsque **false**, les données PictureBullet ne sont pas enregistrées dans le document de sortie. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Saving::DocSaveOptions::get_SavePictureBullet() const
```

## Remarques


Cette option est fournie pour Word 97, qui ne peut pas fonctionner correctement avec les données PictureBullet. Pour supprimer les données PictureBullet, définissez l'option sur \"false\".

## Exemples



Montre comment omettre les données PictureBullet du document lors de l'enregistrement.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Image bullet points.docx");

// Certains traitements de texte, tels que Microsoft Word 97, sont incompatibles avec les données PictureBullet.
// En définissant un indicateur dans l'objet SaveOptions,
// nous pouvons convertir tous les puces d'image en puces ordinaires lors de l'enregistrement.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);
saveOptions->set_SavePictureBullet(false);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.PictureBullets.doc", saveOptions);
```

## Voir aussi

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
