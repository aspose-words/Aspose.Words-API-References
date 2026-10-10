---
title: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages méthode"
linktitle: "ConvertToImages"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages méthode. Convertit les pages du document depuis le flux d'entrée vers un tableau d'images en C++."
type: docs
weight: 2500
url: /fr/cpp/aspose.words/idocumentconverterplugin/converttoimages/
---
## IDocumentConverterPlugin::ConvertToImages method


Convertit les pages d'un document depuis le flux d'entrée en un tableau d'images.

```cpp
virtual System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::IDocumentConverterPlugin::ConvertToImages(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | Le flux d'entrée. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Les options de chargement du document. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | Les options d'enregistrement. |

### ReturnValue

Tableau de flux d'images de pages.

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
