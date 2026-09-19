---
title: "Aspose::Words::LowCode::Merger::MergeToImages metodo"
linktitle: "MergeToImages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::LowCode::Merger::MergeToImages metodo. Unisce i flussi di documenti di input forniti in un unico documento di output utilizzando le opzioni di salvataggio immagine specificate. Renderizza l'output in immagini in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.lowcode/merger/mergetoimages/
---
## Merger::MergeToImages(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Unisce i flussi di documenti di input forniti in un unico documento di output utilizzando le opzioni di salvataggio immagine specificate. Renderizza l'output in immagini.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::SharedPtr<System::IO::Stream>> &inputStreams, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStreams | const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\& | I flussi di file di input. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Le opzioni di salvataggio. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Specifica come unire la formattazione in conflitto. |

## Vedi anche

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::MergeToImages(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Unisce i documenti di input forniti in un unico documento di output utilizzando i nomi di file di input e output specificati e le opzioni di salvataggio. Renderizza l'output in immagini.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::String> &inputFiles, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputFiles | const System::ArrayPtr\<System::String\>\& | I nomi dei file di input. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Le opzioni di salvataggio. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Specifica come unire la formattazione in conflitto. |

## Vedi anche

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
