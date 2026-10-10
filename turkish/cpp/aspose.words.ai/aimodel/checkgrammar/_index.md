---
title: "Aspose::Words::AI::AiModel::CheckGrammar yöntemi"
linktitle: "CheckGrammar"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::AiModel::CheckGrammar yöntemi. Sağlanan belgenin dilbilgisini kontrol eder. Bu işlem, C++'ta belgenin dilbilgisini kontrol etmek için bağlı AI modelini kullanır."
type: docs
weight: 2500
url: /tr/cpp/aspose.words.ai/aimodel/checkgrammar/
---
## AiModel::CheckGrammar method


Sağlanan belgenin dilbilgisini kontrol eder. Bu işlem, belgenin dilbilgisini kontrol etmek için bağlı [AI](../../) modelini kullanır.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::CheckGrammar(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::CheckGrammarOptions> options=nullptr)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Dilbilgisi kontrolü yapılan belge. |
| seçenekler | System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\> | Dilbilgisinin nasıl kontrol edileceğini belirlemek için isteğe bağlı ayarlar. |

### ReturnValue

Dilbilgisi kontrolü yapılmış yeni bir [Document](../../../aspose.words/document/) belgesi.

## Örnekler



Bir belgenin dilbilgisini nasıl kontrol edeceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// OpenAI üretken dil modellerini kullanın.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## Ayrıca Bakınız

* Class [Document](../../../aspose.words/document/)
* Class [CheckGrammarOptions](../../checkgrammaroptions/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
