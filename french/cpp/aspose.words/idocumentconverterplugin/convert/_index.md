---
title: "Méthode Aspose::Words::IDocumentConverterPlugin::Convert"
linktitle: "Convertir"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::IDocumentConverterPlugin::Convert méthode. Convertit le document en utilisant les flux d'entrée et de sortie spécifiés ainsi que les options d'enregistrement en C++."
type: docs
weight: 2000
url: /fr/cpp/aspose.words/idocumentconverterplugin/convert/
---
## IDocumentConverterPlugin::Convert method


Convertit le document en utilisant les flux d'entrée et de sortie spécifiés ainsi que les options d'enregistrement.

```cpp
virtual void Aspose::Words::IDocumentConverterPlugin::Convert(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<System::IO::Stream> outputStream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | Le flux d'entrée. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Les options de chargement du document. |
| outputStream | System::SharedPtr\<System::IO::Stream\> | Le flux de sortie. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | Les options d'enregistrement. |

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
