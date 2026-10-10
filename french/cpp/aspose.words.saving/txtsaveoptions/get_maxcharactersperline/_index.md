---
title: "Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine méthode"
linktitle: "get_MaxCharactersPerLine"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine méthode. Obtient ou définit une valeur entière qui spécifie le nombre maximal de caractères par ligne. La valeur par défaut est 0, ce qui signifie aucune limite en C++."
type: docs
weight: 5000
url: /fr/cpp/aspose.words.saving/txtsaveoptions/get_maxcharactersperline/
---
## TxtSaveOptions::get_MaxCharactersPerLine method


Obtient ou définit une valeur entière qui spécifie le nombre maximal de caractères par ligne. La valeur par défaut est 0, ce qui signifie aucune limite.

```cpp
int32_t Aspose::Words::Saving::TxtSaveOptions::get_MaxCharactersPerLine() const
```


## Exemples



Montre comment définir le nombre maximal de caractères par ligne.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

// Définissez 30 caractères comme maximum autorisé par ligne.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_MaxCharactersPerLine(30);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.MaxCharactersPerLine.txt", saveOptions);
```

## Voir aussi

* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
