---
title: "Méthode Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders"
linktitle: "get_ExportImagesForOldReaders"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders. Spécifie si les mots‑clés pour \"old readers\" sont écrits dans le RTF ou non. Cela peut affecter de manière significative la taille du document RTF. La valeur par défaut est true en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/rtfsaveoptions/get_exportimagesforoldreaders/
---
## RtfSaveOptions::get_ExportImagesForOldReaders method


Spécifie si les mots‑clés pour "old readers" sont écrits dans le RTF ou non. Cela peut affecter significativement la taille du document RTF. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Saving::RtfSaveOptions::get_ExportImagesForOldReaders() const
```

## Remarques


« Old readers » sont des applications antérieures à Microsoft Word 97 ainsi que WordPad. Lorsque cette option est **true**, Aspose.Words écrit des mots‑clés RTF supplémentaires. Ces mots‑clés permettent au document d’être affiché correctement lorsqu’il est ouvert dans une application « old reader », mais peuvent augmenter de façon significative la taille du document.

Si vous définissez cette option sur **false**, seules les images aux formats WMF, EMF et BMP seront affichées dans les « old readers ».

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
