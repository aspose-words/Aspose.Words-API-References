---
title: "Aspose::Words::LowCode::Merger::MergeToImages yöntemi"
linktitle: "MergeToImages"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::LowCode::Merger::MergeToImages yöntemi. Belirtilen görüntü kaydetme seçeneklerini kullanarak verilen giriş belge akışlarını tek bir çıkış belgesine birleştirir. Çıktıyı C++'ta görüntülere render eder."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.lowcode/merger/mergetoimages/
---
## Merger::MergeToImages(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Belirtilen görüntü kaydetme seçeneklerini kullanarak verilen giriş belge akışlarını tek bir çıkış belgesinde birleştirir. Çıktıyı görüntülere render eder.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::SharedPtr<System::IO::Stream>> &inputStreams, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStreams | const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\& | Giriş dosya akışları. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Kaydetme seçenekleri. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

## Ayrıca Bakınız

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::MergeToImages(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Belirtilen giriş ve çıkış dosya adları ve kaydetme seçeneklerini kullanarak verilen giriş belgelerini tek bir çıkış belgesinde birleştirir. Çıktıyı görüntülere render eder.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::String> &inputFiles, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputFiles | const System::ArrayPtr\<System::String\>\& | Giriş dosya adları. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Kaydetme seçenekleri. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Çakışan biçimlendirmelerin nasıl birleştirileceğini belirtir. |

## Ayrıca Bakınız

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
