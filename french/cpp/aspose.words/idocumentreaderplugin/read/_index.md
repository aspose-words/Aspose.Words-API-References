---
title: "Aspose::Words::IDocumentReaderPlugin::Read méthode"
linktitle: "Lire"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::IDocumentReaderPlugin::Read méthode. Lit les données du flux spécifié dans l'instance Document en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words/idocumentreaderplugin/read/
---
## IDocumentReaderPlugin::Read method


Lit les données du flux spécifié dans l'instance [Document](../../document/).

```cpp
virtual void Aspose::Words::IDocumentReaderPlugin::Read(System::SharedPtr<System::IO::Stream> src, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Document> document)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| src | System::SharedPtr\<System::IO::Stream\> | Le flux source à partir duquel lire le document. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Des options de chargement supplémentaires pour charger le document. |
| document | System::SharedPtr\<Aspose::Words::Document\> | L'instance de la classe [Document](../../document/) dans laquelle lire les données. Si l'instance contient du contenu, il sera remplacé par les données du flux source. |

## Voir aussi

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../../document/)
* Interface [IDocumentReaderPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
