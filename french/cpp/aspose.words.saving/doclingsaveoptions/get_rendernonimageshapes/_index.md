---
title: "Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes méthode"
linktitle: "get_RenderNonImageShapes"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes méthode. Obtient ou définit une valeur indiquant si les formes non image doivent être rendues et écrites dans le document JSON Docling de sortie en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/doclingsaveoptions/get_rendernonimageshapes/
---
## DoclingSaveOptions::get_RenderNonImageShapes method


Obtient ou définit une valeur indiquant si les formes non image doivent être rendues et écrites dans le document JSON Docling de sortie.

```cpp
bool Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes() const
```


## Exemples



Montre comment enregistrer un document au format JSON Docling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docling);
// Définissez sur true pour rendre les formes non image et les inclure dans la sortie.
// Définissez sur false (par défaut) pour exclure les formes non image de la sortie.
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```

## Voir aussi

* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
