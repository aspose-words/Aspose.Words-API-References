---
title: "Aspose::Words::AI::AiModel::Translate‑metod"
linktitle: "Översätt"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::AI::AiModel::Translate‑metod. Översätter det angivna dokumentet till det specificerade målspråket. Denna operation utnyttjar den anslutna AI‑modellen för innehållsöversättning i C++."
type: docs
weight: 4667
url: /sv/cpp/aspose.words.ai/aimodel/translate/
---
## AiModel::Translate method


Översätter det angivna dokumentet till det specificerade målspråket. Denna operation utnyttjar den anslutna [AI](../../)‑modellen för innehållsöversättning.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage)=0
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Dokumentet som ska översättas. |
| targetLanguage | Aspose::Words::AI::Language | Språket som dokumentet kommer att översättas till. |

### ReturnValue

Ett nytt [Document](../../../aspose.words/document/) objekt som innehåller det översatta dokumentet.

## Exempel



Visar hur man översätter text med hjälp av Google-modeller.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Använd generativa språkmodeller från Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::GeminiFlashLatest)->WithApiKey(apiKey);

System::SharedPtr<Aspose::Words::Document> translatedDoc = model->Translate(doc, Aspose::Words::AI::Language::Arabic);
translatedDoc->Save(get_ArtifactsDir() + u"AI.AiTranslate.docx");
```

## Se även

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
