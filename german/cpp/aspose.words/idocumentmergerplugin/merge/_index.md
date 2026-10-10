---
title: "Aspose::Words::IDocumentMergerPlugin::Merge-Methode"
linktitle: "Zusammenführen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::IDocumentMergerPlugin::Merge-Methode. Fügt die angegebenen Eingabe-PDF-Dokumente zu einem einzigen Ausgabe-PDF-Dokument zusammen, wobei die angegebenen Eingabe- und Ausgabeströme in C++ verwendet werden."
type: docs
weight: 4000
url: /de/cpp/aspose.words/idocumentmergerplugin/merge/
---
## IDocumentMergerPlugin::Merge method


Führt die angegebenen Eingabe‑PDF‑Dokumente zu einem einzigen Ausgabe‑PDF‑Dokument zusammen, wobei die angegebenen Eingabe‑ und Ausgabeströme verwendet werden.

```cpp
virtual void Aspose::Words::IDocumentMergerPlugin::Merge(System::SharedPtr<System::IO::Stream> outputStream, System::ArrayPtr<System::SharedPtr<System::IO::Stream>> inputStreams, System::ArrayPtr<System::SharedPtr<Aspose::Words::Loading::LoadOptions>> loadOptions)=0
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| outputStream | System::SharedPtr\<System::IO::Stream\> | Der Ausgabestream. |
| inputStreams | System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\> | Die Eingabeströme. |
| loadOptions | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\> | Ladeoptionen für die Eingabedateien. |

## Siehe auch

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Interface [IDocumentMergerPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
