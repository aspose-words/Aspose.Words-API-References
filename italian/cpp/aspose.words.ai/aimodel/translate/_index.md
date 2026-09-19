---
title: "Metodo Aspose::Words::AI::AiModel::Translate"
linktitle: "Traduci"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::AI::AiModel::Translate. Traduce il documento fornito nella lingua di destinazione specificata. Questa operazione sfrutta il modello AI connesso per la traduzione dei contenuti in C++."
type: docs
weight: 4667
url: /it/cpp/aspose.words.ai/aimodel/translate/
---
## AiModel::Translate method


Traduce il documento fornito nella lingua di destinazione specificata. Questa operazione utilizza il modello [AI](../../) connesso per la traduzione del contenuto.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage)=0
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Il documento da tradurre. |
| targetLanguage | Aspose::Words::AI::Language | La lingua in cui il documento sarà tradotto. |

### ReturnValue

Un nuovo oggetto [Document](../../../aspose.words/document/) contenente il documento tradotto.

## Esempi



Mostra come tradurre il testo utilizzando i modelli di Google.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Utilizza i modelli di linguaggio generativo di Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::GeminiFlashLatest)->WithApiKey(apiKey);

System::SharedPtr<Aspose::Words::Document> translatedDoc = model->Translate(doc, Aspose::Words::AI::Language::Arabic);
translatedDoc->Save(get_ArtifactsDir() + u"AI.AiTranslate.docx");
```

## Vedi anche

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
