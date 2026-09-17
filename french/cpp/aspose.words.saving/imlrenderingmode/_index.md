---
title: "Aspose::Words::Saving::ImlRenderingMode enum"
linktitle: "ImlRenderingMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::ImlRenderingMode enum. Spécifie comment les objets encre (InkML) sont rendus aux formats de page fixe en C++."
type: docs
weight: 66000
url: /fr/cpp/aspose.words.saving/imlrenderingmode/
---
## ImlRenderingMode enum


Spécifie comment les objets encre (InkML) sont rendus aux formats de page fixe.

```cpp
enum class ImlRenderingMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Fallback | 0 | Si une forme de repli est disponible pour l’objet encre (InkML), Aspose.Words rend la forme de repli à la place de l’InkML. |
| InkML | 1 | Aspose.Words ignore la forme de secours de l'objet d'encre (InkML) et rend InkML lui-même. C'est le mode par défaut. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
