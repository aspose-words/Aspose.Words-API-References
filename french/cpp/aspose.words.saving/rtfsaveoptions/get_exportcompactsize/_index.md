---
title: "Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize méthode"
linktitle: "get_ExportCompactSize"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize méthode. Permet de réduire la taille des documents RTF en sortie, mais si ceux-ci contiennent du texte RTL (de droite à gauche), il ne sera pas affiché correctement. La valeur par défaut est false en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/rtfsaveoptions/get_exportcompactsize/
---
## RtfSaveOptions::get_ExportCompactSize method


Permet de réduire la taille des documents RTF en sortie, mais s’ils contiennent du texte RTL (de droite à gauche), il ne sera pas affiché correctement. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportCompactSize() const
```

## Remarques


Si le document que vous souhaitez convertir en RTF avec Aspose.Words ne contient pas de texte de droite à gauche dans des langues comme l'arabe, vous pouvez régler cette option sur **true** pour réduire la taille du RTF résultant.

## Exemples



Montre comment enregistrer un document au format .rtf avec des options personnalisées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

// Créez un objet "RtfSaveOptions" à transmettre à la méthode "Save" du document afin de modifier la façon dont nous l'enregistrons au format RTF.
auto options = System::MakeObject<Aspose::Words::Saving::RtfSaveOptions>();

ASSERT_EQ(Aspose::Words::SaveFormat::Rtf, options->get_SaveFormat());

// Définissez la propriété "ExportCompactSize" sur "true" pour
// réduire la taille du document enregistré au détriment de la compatibilité du texte de droite à gauche.
options->set_ExportCompactSize(true);

// Définissez la propriété "ExportImagesFotOldReaders" sur "true" pour utiliser des mots-clés supplémentaires afin de garantir que notre document est
// compatible avec les lecteurs antérieurs à Microsoft Word 97 et WordPad.
// Définissez la propriété "ExportImagesFotOldReaders" sur "false" pour réduire la taille du document,
// mais empêcher les anciens lecteurs de pouvoir lire les images non-métasignées ou BMP que le document pourrait contenir.
options->set_ExportImagesForOldReaders(exportImagesForOldReaders);

doc->Save(get_ArtifactsDir() + u"RtfSaveOptions.ExportImages.rtf", options);
```

## Voir aussi

* Class [RtfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
