---
title: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode méthode"
linktitle: "get_ImlRenderingMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode méthode. Obtient ou définit une valeur déterminant comment les objets d'encre (InkML) sont rendus en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.saving/saveoptions/get_imlrenderingmode/
---
## SaveOptions::get_ImlRenderingMode method


Obtient ou définit une valeur déterminant comment les objets encre (InkML) sont rendus.

```cpp
Aspose::Words::Saving::ImlRenderingMode Aspose::Words::Saving::SaveOptions::get_ImlRenderingMode() const
```

## Remarques


La valeur par défaut est [InkML](../../imlrenderingmode/).

Cette propriété est utilisée lorsque le document est exporté vers des formats de page fixe.

## Exemples



Montre comment rendre l'objet Ink.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Ink object.docx");

// Définir 'ImlRenderingMode.InkML' ignore la forme de secours de l'objet d'encre (InkML) et rend InkML lui-même.
// Si le résultat du rendu est insatisfaisant,
// veuillez utiliser 'ImlRenderingMode.Fallback' pour obtenir un résultat similaire aux versions précédentes.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
saveOptions->set_ImlRenderingMode(Aspose::Words::Saving::ImlRenderingMode::InkML);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.RenderInkObject.jpeg", saveOptions);
```

## Voir aussi

* Enum [ImlRenderingMode](../../imlrenderingmode/)
* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
