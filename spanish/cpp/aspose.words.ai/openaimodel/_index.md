---
title: "Aspose::Words::AI::OpenAiModel clase"
linktitle: "OpenAiModel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::AI::OpenAiModel clase. Clase que representa la integración de modelos OpenAi dentro de Aspose.Words en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.ai/openaimodel/
---
## OpenAiModel class


Clase que representa la integración de modelos OpenAi dentro de [Aspose.Words](../../aspose.words/).

```cpp
class OpenAiModel : public Aspose::Words::AI::AiModel
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Comprueba la gramática del documento proporcionado. Esta operación aprovecha el modelo de [AI](../) conectado para comprobar la gramática del documento. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Crea una nueva instancia de la clase [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Obtiene o establece el número de milisegundos a esperar antes de que la solicitud al modelo [AI](../) expire. El valor predeterminado es 100,000 milisegundos (100 segundos). |
| [get_Url](./get_url/)() override | Obtiene una URL del modelo. El valor predeterminado es "https://api.openai.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OpenAiModel](./openaimodel/)(const System::String\&, const System::String\&) | Inicializa una nueva instancia de la clase [OpenAiModel](./). |
| [OpenAiModel](./openaimodel/)(const System::String\&) | Inicializa una nueva instancia de la clase [OpenAiModel](./). |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Método setter para [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Establece una URL del modelo. El valor predeterminado es "https://api.openai.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Genera un resumen del documento especificado, con opciones para ajustar la longitud del resumen. Esta operación utiliza el modelo [AI](../) conectado para el procesamiento del contenido. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Genera resúmenes para una matriz de documentos, con opciones para controlar la longitud del resumen y otras configuraciones. Este método utiliza el modelo [AI](../) conectado para procesar cada documento en la matriz. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Traduce el documento proporcionado al idioma de destino especificado. Esta operación utiliza el modelo [AI](../) conectado para la traducción del contenido. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Establece una clave API especificada al modelo. |
| [WithOrganization](./withorganization/)(const System::String\&) | Establece una Organización especificada al modelo. |
| [WithProject](./withproject/)(const System::String\&) | Establece un Proyecto especificado al modelo. |

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

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
