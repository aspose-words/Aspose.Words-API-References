---
title: "Метод Aspose::Words::AI::AiModel::Translate"
linktitle: "Перевести"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::AI::AiModel::Translate. Переводит предоставленный документ на указанный целевой язык. Эта операция использует подключенную AI‑модель для перевода контента в C++."
type: docs
weight: 4667
url: /ru/cpp/aspose.words.ai/aimodel/translate/
---
## AiModel::Translate method


Переводит предоставленный документ на указанный целевой язык. Эта операция использует подключённую модель [AI](../../) для перевода контента.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Документ для перевода. |
| targetLanguage | Aspose::Words::AI::Language | Язык, на который будет переведен документ. |

### ReturnValue

Новый объект [Document](../../../aspose.words/document/), содержащий переведённый документ.

## Примеры



Показывает, как переводить текст с помощью моделей Google.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// Используйте генеративные языковые модели Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::GeminiFlashLatest)->WithApiKey(apiKey);

System::SharedPtr<Aspose::Words::Document> translatedDoc = model->Translate(doc, Aspose::Words::AI::Language::Arabic);
translatedDoc->Save(get_ArtifactsDir() + u"AI.AiTranslate.docx");
```

## См. также

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
