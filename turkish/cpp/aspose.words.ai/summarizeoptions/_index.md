---
title: "Aspose::Words::AI::SummarizeOptions sınıfı"
linktitle: "SummarizeOptions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::AI::SummarizeOptions sınıfı. C++'ta belge içeriğini özetlemek için çeşitli seçenekleri belirtmenizi sağlar."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class


Belge içeriğini özetlemek için çeşitli seçenekleri belirtmeye olanak tanır.

```cpp
class SummarizeOptions : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_SummaryLength](./get_summarylength/)() const | Özet uzunluğunu belirtmenizi sağlar. Varsayılan değer [Medium](../summarylength/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SummaryLength](./set_summarylength/)(Aspose::Words::AI::SummaryLength) | Ayarlayıcı, [Aspose::Words::AI::SummarizeOptions::get_SummaryLength](./get_summarylength/) için. |
| [SummarizeOptions](./summarizeoptions/)() | Yeni bir [SummarizeOptions](./) sınıf örneği başlatır. |
| static [Type](./type/)() |  |

## Örnekler



OpenAI ve Google modellerini kullanarak metni nasıl özetleyeceğinizi gösterir.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// OpenAI veya Google üretken dil modellerini kullanın.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
