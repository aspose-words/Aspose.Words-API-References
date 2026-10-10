---
title: "Aspose::Words::LowCode::Merger::MergeToImages metod"
linktitle: "MergeToImages"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::LowCode::Merger::MergeToImages metod. Slår samman de angivna inmatningsdokumentströmmarna till ett enda utdokument med angivna bildsparalternativ. Renderar utdatan till bilder i C++."
type: docs
weight: 2000
url: /sv/cpp/aspose.words.lowcode/merger/mergetoimages/
---
## Merger::MergeToImages(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Slår samman de angivna indatadokumentströmarna till ett enda utdata-dokument med angivna bildsparalternativ. Renderar utdata till bilder.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::SharedPtr<System::IO::Stream>> &inputStreams, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStreams | const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\& | Inmatningsfilströmmarna. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Sparalternativen. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Anger hur formatering som krockar ska slås samman. |

## Se även

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::MergeToImages(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Slår samman de angivna indatadokumenten till ett enda utdata-dokument med angivna in- och utfilnamn samt sparalternativ. Renderar utdata till bilder.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::String> &inputFiles, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFiles | const System::ArrayPtr\<System::String\>\& | Inmatningsfilnamnen. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Sparalternativen. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Anger hur formatering som krockar ska slås samman. |

## Se även

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
