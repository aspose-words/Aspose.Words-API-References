---
title: "Aspose::Words::AI::AiModelType enumeración"
linktitle: "AiModelType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::AI::AiModelType enumeración. Representa los tipos de AiModel que pueden integrarse en el flujo de trabajo de procesamiento de documentos en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.ai/aimodeltype/
---
## AiModelType enum


Representa los tipos de [AiModel](../aimodel/) que pueden integrarse en el flujo de trabajo de procesamiento de documentos.

```cpp
enum class AiModelType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Gpt4O | 0 | Tipo de modelo generativo GPT-4o. |
| Gpt4OMini | 1 | Tipo de modelo generativo GPT-4o mini. |
| Gpt4Turbo | 2 | Tipo de modelo generativo GPT-4 Turbo. |
| Gpt35Turbo | 3 | Tipo de modelo generativo GPT-3.5 Turbo. |
| GeminiFlashLatest | 4 | Tipo de modelo generativo Gemini Flash de la última versión. |
| GeminiProLatest | 6 | Tipo de modelo generativo Gemini Pro de la última versión. |
| Claude35Sonnet | 7 | Claude 3.5 Sonnet tipo de modelo generativo. |
| Claude35Haiku | 8 | Claude 3.5 Haiku tipo de modelo generativo. |
| Claude3Opus | 9 | Claude 3 Opus tipo de modelo generativo. |
| Claude3Sonnet | 10 | Claude 3 Sonnet tipo de modelo generativo. |
| Claude3Haiku | 11 | Claude 3 Haiku tipo de modelo generativo. |


## Ejemplos



Muestra cómo resumir texto usando los modelos de OpenAI y Google.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Utiliza los modelos de lenguaje generativo de OpenAI o Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```

## Ver también

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
