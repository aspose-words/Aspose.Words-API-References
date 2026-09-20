---
title: "Método Aspose::Words::AI::AiModel::Translate"
linktitle: "Traducir"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::AI::AiModel::Translate. Traduce el documento proporcionado al idioma de destino especificado. Esta operación aprovecha el modelo de IA conectado para traducir contenido en C++."
type: docs
weight: 4667
url: /es/cpp/aspose.words.ai/aimodel/translate/
---
## AiModel::Translate method


Traduce el documento proporcionado al idioma objetivo especificado. Esta operación aprovecha el modelo [AI](../../) conectado para la traducción de contenido.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | El documento a traducir. |
| targetLanguage | Aspose::Words::AI::Language | El idioma al que se traducirá el documento. |

### ReturnValue

Un nuevo objeto [Document](../../../aspose.words/document/) que contiene el documento traducido.

## Ejemplos



Muestra cómo traducir texto usando los modelos de Google.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Utiliza los modelos de lenguaje generativo de Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::GeminiFlashLatest)->WithApiKey(apiKey);

System::SharedPtr<Aspose::Words::Document> translatedDoc = model->Translate(doc, Aspose::Words::AI::Language::Arabic);
translatedDoc->Save(get_ArtifactsDir() + u"AI.AiTranslate.docx");
```

## Ver también

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
