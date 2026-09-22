---
title: "Aspose::Words::AI::OpenAiModel::OpenAiModel yapıcı"
linktitle: "OpenAiModel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::OpenAiModel::OpenAiModel yapıcı. C++'ta OpenAiModel sınıfının yeni bir örneğini başlatır."
type: docs
weight: 1334
url: /tr/cpp/aspose.words.ai/openaimodel/openaimodel/
---
## OpenAiModel::OpenAiModel(const System::String\&) constructor


[OpenAiModel](../) sınıfının yeni bir örneğini başlatır.

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Modelin adı. Örneğin, gpt-5.2-chat-latest. |

## Ayrıca Bakınız

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::OpenAiModel(const System::String\&, const System::String\&) constructor


[OpenAiModel](../) sınıfının yeni bir örneğini başlatır.

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name, const System::String &apiKey)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Modelin adı. Örneğin, gpt-5.2-chat-latest. |
| apiKey | const System::String\& | OpenAi API'sini kullanmak için API anahtarı. |

## Örnekler



Bir API anahtarı ve model adı kullanarak OpenAI model örneğini doğrudan oluşturmayı gösterir.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Model adı ve API anahtarıyla yapıcıyı kullanarak bir OpenAI model örneği oluşturun.
auto model = System::MakeObject<Aspose::Words::AI::OpenAiModel>(u"gpt-4o-mini", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
// Kısa özet uzunluğuyla OpenAI modelini kullanarak belgeyi özetleyin.
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);

summary->Save(get_ArtifactsDir() + u"OpenAiModel.OpenAiModelConstructor.docx");
```

## Ayrıca Bakınız

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
