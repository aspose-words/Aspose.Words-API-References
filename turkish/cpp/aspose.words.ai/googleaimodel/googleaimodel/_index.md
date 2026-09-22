---
title: "Aspose::Words::AI::GoogleAiModel::GoogleAiModel yapıcı"
linktitle: "GoogleAiModel"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::GoogleAiModel::GoogleAiModel yapıcı. C++'ta GoogleAiModel sınıfının yeni bir örneğini başlatır."
type: docs
weight: 1500
url: /tr/cpp/aspose.words.ai/googleaimodel/googleaimodel/
---
## GoogleAiModel::GoogleAiModel(const System::String\&) constructor


[GoogleAiModel](../) sınıfının yeni bir örneğini başlatır.

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Modelin adı. Örneğin, gemini-2.5-flash. |

## Örnekler



Google [AI](../../) modelini nasıl kullanacağınızı gösterir.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Ayrıca Bakınız

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## GoogleAiModel::GoogleAiModel(const System::String\&, const System::String\&) constructor


[GoogleAiModel](../) sınıfının yeni bir örneğini başlatır.

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name, const System::String &apiKey)
```


| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | const System::String\& | Modelin adı. Örneğin, gemini-2.5-flash. |
| apiKey | const System::String\& | Gemini API'sini kullanmak için API anahtarı. Ayrıntılar için lütfen [https://ai.google.dev/gemini-api/docs/api-key](https://ai.google.dev/gemini-api/docs/api-key) adresine bakın. |

## Örnekler



Google [AI](../../) modelini nasıl kullanacağınızı gösterir.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## Ayrıca Bakınız

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
