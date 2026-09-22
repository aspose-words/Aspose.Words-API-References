---
title: "Aspose::Words::IDocumentMergerPlugin::Merge yöntemi"
linktitle: "Merge"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::IDocumentMergerPlugin::Merge yöntemi. Belirtilen giriş ve çıkış akışlarını kullanarak verilen PDF giriş belgelerini tek bir PDF çıkış belgesine birleştirir C++'ta."
type: docs
weight: 4000
url: /tr/cpp/aspose.words/idocumentmergerplugin/merge/
---
## IDocumentMergerPlugin::Merge method


Belirtilen giriş ve çıkış akışlarını kullanarak verilen giriş PDF belgelerini tek bir çıkış PDF belgesine birleştirir.

```cpp
virtual void Aspose::Words::IDocumentMergerPlugin::Merge(System::SharedPtr<System::IO::Stream> outputStream, System::ArrayPtr<System::SharedPtr<System::IO::Stream>> inputStreams, System::ArrayPtr<System::SharedPtr<Aspose::Words::Loading::LoadOptions>> loadOptions)=0
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| outputStream | System::SharedPtr\<System::IO::Stream\> | Çıktı akışı. |
| inputStreams | System::ArrayPtr\\<System::SharedPtr\\<System::IO::Stream\\>\\> | Giriş akışları. |
| loadOptions | System::ArrayPtr\\<System::SharedPtr\\<Aspose::Words::Loading::LoadOptions\\>\\> | Giriş dosyaları için yükleme seçenekleri. |

## Ayrıca Bakınız

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Interface [IDocumentMergerPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
