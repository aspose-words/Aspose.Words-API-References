---
title: "Enumeración Aspose::Words::AI::SummaryLength"
linktitle: "SummaryLength"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Enumeración Aspose::Words::AI::SummaryLength. Enumera las posibles longitudes del resumen en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.ai/summarylength/
---
## SummaryLength enum


Enumera las posibles longitudes del resumen.

```cpp
enum class SummaryLength
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| VeryShort | 0 | Intenta generar 1-2 oraciones. |
| Short | 1 | Intenta generar 3-4 oraciones. |
| Medium | 2 | Intenta generar 5-6 oraciones. |
| Largo | 3 | Intenta generar 7-10 oraciones. |
| MuyLargo | 4 | Intenta generar 11-20 oraciones. |


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
