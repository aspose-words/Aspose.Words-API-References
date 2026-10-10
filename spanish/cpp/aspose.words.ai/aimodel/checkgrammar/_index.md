---
title: "Método Aspose::Words::AI::AiModel::CheckGrammar"
linktitle: "CheckGrammar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::AI::AiModel::CheckGrammar. Verifica la gramática del documento proporcionado. Esta operación utiliza el modelo de AI conectado para comprobar la gramática del documento en C++."
type: docs
weight: 2500
url: /es/cpp/aspose.words.ai/aimodel/checkgrammar/
---
## AiModel::CheckGrammar method


Verifica la gramática del documento proporcionado. Esta operación utiliza el modelo de [AI](../../) conectado para comprobar la gramática del documento.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::CheckGrammar(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::CheckGrammarOptions> options=nullptr)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | El documento que se está verificando para gramática. |
| opciones | System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\> | Configuraciones opcionales para controlar cómo se verificará la gramática. |

### ReturnValue

Un nuevo [Document](../../../aspose.words/document/) con gramática verificada.

## Ejemplos



Muestra cómo comprobar la gramática de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Utiliza modelos de lenguaje generativo de OpenAI.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## Ver también

* Class [Document](../../../aspose.words/document/)
* Class [CheckGrammarOptions](../../checkgrammaroptions/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
