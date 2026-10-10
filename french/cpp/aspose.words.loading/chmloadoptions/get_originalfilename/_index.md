---
title: "Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName méthode"
linktitle: "get_OriginalFileName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName méthode. Le nom du fichier CHM. La valeur par défaut est null en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.loading/chmloadoptions/get_originalfilename/
---
## ChmLoadOptions::get_OriginalFileName method


Le nom du fichier CHM. La valeur par défaut est **null**.

```cpp
System::String Aspose::Words::Loading::ChmLoadOptions::get_OriginalFileName() const
```

## Remarques


Les documents CHM peuvent contenir des liens qui font référence au même document par son nom de fichier. Aspose.Words prend en charge ces liens et utilise généralement [OriginalFileName](../../../aspose.words/document/get_originalfilename/) pour vérifier si le fichier référencé par un lien est le fichier en cours de chargement. Si un document est chargé à partir d'un flux, son nom de fichier d'origine doit être spécifié explicitement via cette propriété, car il ne peut pas être déterminé automatiquement.

Si un document CHM est chargé à partir d'un fichier et qu'une valeur non nulle pour cette propriété est spécifiée, cette valeur aura la priorité sur le nom réel du fichier stocké dans [OriginalFileName](../../../aspose.words/document/get_originalfilename/).

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
