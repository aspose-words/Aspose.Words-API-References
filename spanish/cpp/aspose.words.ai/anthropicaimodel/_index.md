---
title: "Clase Aspose::Words::AI::AnthropicAiModel"
linktitle: "AnthropicAiModel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::AI::AnthropicAiModel. Una clase abstracta que representa la integración con los modelos de AI de Anthropic dentro de Aspose.Words en C++."
type: docs
weight: 1250
url: /es/cpp/aspose.words.ai/anthropicaimodel/
---
## AnthropicAiModel class


Una clase abstracta que representa la integración con los modelos de [AI](../) de Anthropic dentro de [Aspose.Words](../../aspose.words/).

```cpp
class AnthropicAiModel : public Aspose::Words::AI::AiModel
```

## Métodos

| Método | Descripción |
| --- | --- |
| [AnthropicAiModel](./anthropicaimodel/)() |  |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | Comprueba la gramática del documento proporcionado. Esta operación aprovecha el modelo de [AI](../) conectado para comprobar la gramática del documento. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | Crea una nueva instancia de la clase [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | Obtiene o establece el número de milisegundos a esperar antes de que la solicitud al modelo [AI](../) expire. El valor predeterminado es 100,000 milisegundos (100 segundos). |
| [get_Url](./get_url/)() override | Obtiene una URL del modelo. El valor predeterminado es "https://api.anthropic.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | Método setter para [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | Establece una URL del modelo. El valor predeterminado es "https://api.anthropic.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Genera un resumen del documento especificado, con opciones para ajustar la longitud del resumen. Esta operación utiliza el modelo [AI](../) conectado para el procesamiento del contenido. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | Genera resúmenes para una matriz de documentos, con opciones para controlar la longitud del resumen y otras configuraciones. Este método utiliza el modelo [AI](../) conectado para procesar cada documento en la matriz. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | Traduce el documento proporcionado al idioma de destino especificado. Esta operación utiliza el modelo [AI](../) conectado para la traducción del contenido. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | Establece una clave API especificada al modelo. |
## Ver también

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
