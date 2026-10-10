---
title: "Méthode Aspose::Words::Saving::PclSaveOptions::AddPrinterFont"
linktitle: "AddPrinterFont"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::PclSaveOptions::AddPrinterFont. Ajoute des informations sur la police qui est téléchargée sur l'imprimante par le fabricant en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions::AddPrinterFont method


Ajoute des informations sur la police qui est téléchargée sur l'imprimante par le fabricant.

```cpp
void Aspose::Words::Saving::PclSaveOptions::AddPrinterFont(const System::String &fontFullName, const System::String &fontPclName)
```


| Paramètre | Type | Description |
| --- | --- | --- |
| fontFullName | const System::String\& | Nom complet de la police (par ex. "Times New Roman Bold Italic"). |
| fontPclName | const System::String\& | Nom de la police utilisée dans le document Pcl. |

## Exemples



Montre comment faire en sorte qu'une imprimante substitue toutes les occurrences d'une police spécifique par une autre police.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Courier");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->AddPrinterFont(u"Courier New", u"Courier");

// Lors de l'impression de ce document, l'imprimante utilisera la police "Courier New"
// pour accéder aux parties où notre document utilisait la police "Courier".
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

## Voir aussi

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
