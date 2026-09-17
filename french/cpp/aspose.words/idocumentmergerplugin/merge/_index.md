---
title: "Aspose::Words::IDocumentMergerPlugin::Merge méthode"
linktitle: "Fusionner"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::IDocumentMergerPlugin::Merge méthode. Fusionne les documents PDF d'entrée fournis en un seul document PDF de sortie en utilisant les flux d'entrée et de sortie spécifiés en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/idocumentmergerplugin/merge/
---
## IDocumentMergerPlugin::Merge method


Fusionne les documents PDF d’entrée fournis en un seul document PDF de sortie en utilisant les flux d’entrée et de sortie spécifiés.

```cpp
virtual void Aspose::Words::IDocumentMergerPlugin::Merge(System::SharedPtr<System::IO::Stream> outputStream, System::ArrayPtr<System::SharedPtr<System::IO::Stream>> inputStreams, System::ArrayPtr<System::SharedPtr<Aspose::Words::Loading::LoadOptions>> loadOptions)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| outputStream | System::SharedPtr\<System::IO::Stream\> | Le flux de sortie. |
| inputStreams | System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\> | Les flux d'entrée. |
| loadOptions | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\> | Options de chargement pour les fichiers d'entrée. |

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Interface [IDocumentMergerPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
