---
title: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions constructeur"
linktitle: "ChmLoadOptions"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions constructeur. Initialise une nouvelle instance de cette classe avec des valeurs par défaut en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions::ChmLoadOptions constructor


Initialise une nouvelle instance de cette classe avec les valeurs par défaut.

```cpp
Aspose::Words::Loading::ChmLoadOptions::ChmLoadOptions()
```


## Exemples



Montre comment résoudre les URL comme "ms-its:myfile.chm::/index.htm".
```cpp
// Notre document contient des URL comme "ms-its:amhelp.chm::....htm", mais il a un nom différent,
// Les liens de fichiers .so ne fonctionnent pas après les avoir enregistrés en HTML.
// Nous devons définir le nom de fichier d'origine dans 'ChmLoadOptions' pour éviter ce comportement.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::ChmLoadOptions>();
loadOptions->set_OriginalFileName(u"amhelp.chm");

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::IO::File::ReadAllBytes(get_MyDir() + u"Document with ms-its links.chm")), loadOptions);

doc->Save(get_ArtifactsDir() + u"ExChmLoadOptions.OriginalFileName.html");
```

## Voir aussi

* Class [ChmLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
