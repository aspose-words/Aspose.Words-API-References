---
title: "Aspose::Words::AI::AnthropicAiModel::Summarize metodu"
linktitle: "Özetle"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::AnthropicAiModel::Summarize metodu. Belgeler dizisi için özetler oluşturur, özet uzunluğunu ve diğer ayarları kontrol etme seçenekleriyle. Bu metod, dizideki her belgeyi işlemek için bağlı AI modelini C++'da kullanır."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.ai/anthropicaimodel/summarize/
---
## AnthropicAiModel::Summarize(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Belgeler dizisi için özetler oluşturur, özet uzunluğunu ve diğer ayarları kontrol etme seçenekleriyle. Bu metod, dizideki her belgeyi işlemek için bağlı [AI](../../) modelini kullanır.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AnthropicAiModel::Summarize(System::ArrayPtr<System::SharedPtr<Aspose::Words::Document>> sourceDocuments, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocuments | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\> | Özetlenecek belgelerden oluşan bir dizi. |
| seçenekler | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Özet uzunluğunu ve diğer parametreleri kontrol etmek için isteğe bağlı ayarlar |

### ReturnValue

Belgenin içeriğinin özetlenmiş bir versiyonu.

## Ayrıca Bakınız

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [AnthropicAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## AnthropicAiModel::Summarize(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Belirtilen belgenin bir özetini oluşturur, özetin uzunluğunu ayarlamak için seçenekler sunar. Bu işlem, içerik işleme için bağlı [AI](../../) modelini kullanır.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AnthropicAiModel::Summarize(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Özetlenecek belge. |
| seçenekler | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Özet uzunluğunu ve diğer parametreleri kontrol etmek için isteğe bağlı ayarlar. |

### ReturnValue

Belgenin içeriğinin özetlenmiş bir versiyonu.

## Ayrıca Bakınız

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [AnthropicAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
