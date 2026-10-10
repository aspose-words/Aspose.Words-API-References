---
title: "Aspose::Words::AI::SummarizeOptions clase"
linktitle: "SummarizeOptions"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::AI::SummarizeOptions clase. Permite especificar varias opciones para resumir el contenido del documento en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words.ai/summarizeoptions/
---
## SummarizeOptions class


Permite especificar varias opciones para resumir el contenido del documento.

```cpp
class SummarizeOptions : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_SummaryLength](./get_summarylength/)() const | Permite especificar la longitud del resumen. El valor predeterminado es [Medium](../summarylength/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SummaryLength](./set_summarylength/)(Aspose::Words::AI::SummaryLength) | Método setter para [Aspose::Words::AI::SummarizeOptions::get_SummaryLength](./get_summarylength/). |
| [SummarizeOptions](./summarizeoptions/)() | Inicializa una nueva instancia de la clase [SummarizeOptions](./). |
| static [Type](./type/)() |  |

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
