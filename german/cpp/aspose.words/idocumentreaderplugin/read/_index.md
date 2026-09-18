---
title: "Aspose::Words::IDocumentReaderPlugin::Read-Methode"
linktitle: "Lesen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::IDocumentReaderPlugin::Read-Methode. Liest die Daten aus dem angegebenen Stream in die Document-Instanz in C++ ein."
type: docs
weight: 4000
url: /de/cpp/aspose.words/idocumentreaderplugin/read/
---
## IDocumentReaderPlugin::Read method


Liest die Daten aus dem angegebenen Stream in die [Document](../../document/) Instanz.

```cpp
virtual void Aspose::Words::IDocumentReaderPlugin::Read(System::SharedPtr<System::IO::Stream> src, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Document> document)=0
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| src | System::SharedPtr\<System::IO::Stream\> | Der Quell-Stream, aus dem das Dokument gelesen wird. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Zusätzliche Ladeoptionen zum Laden des Dokuments. |
| document | System::SharedPtr\<Aspose::Words::Document\> | Die Instanz der [Document](../../document/)-Klasse, in die die Daten gelesen werden sollen. Wenn die Instanz bereits Inhalt enthält, wird dieser durch die Daten aus dem Quell-Stream überschrieben. |

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../../document/)
* Interface [IDocumentReaderPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
