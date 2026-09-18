---
title: "Aspose::Words::AI::AiModel::Translate Methode"
linktitle: "Übersetzen"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::AI::AiModel::Translate Methode. Übersetzt das bereitgestellte Dokument in die angegebene Zielsprache. Dieser Vorgang nutzt das verbundene KI‑Modell zur Inhaltsübersetzung in C++."
type: docs
weight: 4667
url: /de/cpp/aspose.words.ai/aimodel/translate/
---
## AiModel::Translate method


Übersetzt das bereitgestellte Dokument in die angegebene Zielsprache. Dieser Vorgang nutzt das verbundene [AI](../../)-Modell zum Übersetzen von Inhalten.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage)=0
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Das zu übersetzende Dokument. |
| targetLanguage | Aspose::Words::AI::Language | Die Sprache, in die das Dokument übersetzt wird. |

### ReturnValue

Ein neues [Document](../../../aspose.words/document/)-Objekt, das das übersetzte Dokument enthält.

## Beispiele



Zeigt, wie man Text mit Google‑Modellen übersetzt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Verwenden Sie generative Sprachmodelle von Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::GeminiFlashLatest)->WithApiKey(apiKey);

System::SharedPtr<Aspose::Words::Document> translatedDoc = model->Translate(doc, Aspose::Words::AI::Language::Arabic);
translatedDoc->Save(get_ArtifactsDir() + u"AI.AiTranslate.docx");
```

## Siehe auch

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
