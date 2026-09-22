---
title: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages method"
linktitle: "ConvertToImages"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages method. Belge sayfalarını giriş akışından görüntü dizisine C++'ta dönüştürür."
type: docs
weight: 2500
url: /tr/cpp/aspose.words/idocumentconverterplugin/converttoimages/
---
## IDocumentConverterPlugin::ConvertToImages method


Belgeden sayfaları giriş akışından görüntü dizisine dönüştürür.

```cpp
virtual System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::IDocumentConverterPlugin::ConvertToImages(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | Giriş akışı. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Belge yükleme seçenekleri. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | Kaydetme seçenekleri. |

### ReturnValue

Sayfa görüntüsü akışlarının dizisi.

## Ayrıca Bakınız

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
