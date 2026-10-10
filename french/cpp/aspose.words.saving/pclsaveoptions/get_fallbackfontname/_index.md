---
title: "Méthode Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName"
linktitle: "get_FallbackFontName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName. Nom de la police qui sera utilisée si aucune police attendue n’est trouvée dans les collections d’imprimante et de polices intégrées en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/pclsaveoptions/get_fallbackfontname/
---
## PclSaveOptions::get_FallbackFontName method


Nom de la police qui sera utilisée si aucune police attendue n'est trouvée dans l'imprimante et les collections de polices intégrées.

```cpp
System::String Aspose::Words::Saving::PclSaveOptions::get_FallbackFontName() const
```


## Exemples



Montre comment déclarer une police que l’imprimante appliquera au texte imprimé comme substitut si la police d’origine n’est pas disponible.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Non-existent font");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->set_FallbackFontName(u"Times New Roman");

// Ce document indiquera à l’imprimante d’appliquer "Times New Roman" au texte dont la police est manquante.
// Si "Times New Roman" est également indisponible, l’imprimante utilisera par défaut la police "Arial".
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.SetPrinterFont.pcl", saveOptions);
```

## Voir aussi

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
