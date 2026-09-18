---
title: "Aspose::Words::LowCode::Merger::MergeToImages-Methode"
linktitle: "MergeToImages"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::LowCode::Merger::MergeToImages-Methode. Fügt die angegebenen Eingabedokument-Streams zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Bildspeicheroptionen verwendet werden. Rendert die Ausgabe zu Bildern in C++."
type: docs
weight: 2000
url: /de/cpp/aspose.words.lowcode/merger/mergetoimages/
---
## Merger::MergeToImages(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Führt die angegebenen Eingabedokumentströme zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Bildspeicheroptionen verwendet werden. Rendert die Ausgabe zu Bildern.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::SharedPtr<System::IO::Stream>> &inputStreams, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputStreams | const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\& | Die Eingabedatei-Streams. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Die Speicheroptionen. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Gibt an, wie Formatierungen, die kollidieren, zusammengeführt werden. |

## Siehe auch

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::MergeToImages(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Führt die angegebenen Eingabedokumente zu einem einzigen Ausgabedokument zusammen, wobei die angegebenen Eingabe- und Ausgabedateinamen und Speicheroptionen verwendet werden. Rendert die Ausgabe zu Bildern.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::String> &inputFiles, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| inputFiles | const System::ArrayPtr\<System::String\>\& | Die Eingabedateinamen. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Die Speicheroptionen. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Gibt an, wie Formatierungen, die kollidieren, zusammengeführt werden. |

## Siehe auch

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
