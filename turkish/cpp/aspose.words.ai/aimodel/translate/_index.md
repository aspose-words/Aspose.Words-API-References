---
title: "Aspose::Words::AI::AiModel::Translate yöntemi"
linktitle: "Çevir"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::AiModel::Translate yöntemi. Sağlanan belgeyi belirtilen hedef dile çevirir. Bu işlem, C++'da içerik çevirisi için bağlı AI modelini kullanır."
type: docs
weight: 4667
url: /tr/cpp/aspose.words.ai/aimodel/translate/
---
## AiModel::Translate method


Sağlanan belgeyi belirtilen hedef dile çevirir. Bu işlem, içerik çevirisi için bağlı [AI](../../) modelini kullanır.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage)=0
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Çevrilecek belge. |
| targetLanguage | Aspose::Words::AI::Language | Belgenin çevrileceği dil. |

### ReturnValue

Çevrilen belgeyi içeren yeni bir [Document](../../../aspose.words/document/) nesnesi.

## Örnekler



Google modellerini kullanarak metni nasıl çevireceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Google üretken dil modellerini kullanın.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::GeminiFlashLatest)->WithApiKey(apiKey);

System::SharedPtr<Aspose::Words::Document> translatedDoc = model->Translate(doc, Aspose::Words::AI::Language::Arabic);
translatedDoc->Save(get_ArtifactsDir() + u"AI.AiTranslate.docx");
```

## Ayrıca Bakınız

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
