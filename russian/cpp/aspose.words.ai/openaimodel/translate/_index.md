---
title: "Метод Aspose::Words::AI::OpenAiModel::Translate"
linktitle: "Перевести"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::AI::OpenAiModel::Translate. Переводит предоставленный документ на указанный целевой язык. Эта операция использует подключённую AI‑модель для перевода контента на C++."
type: docs
weight: 3667
url: /ru/cpp/aspose.words.ai/openaimodel/translate/
---
## OpenAiModel::Translate method


Переводит предоставленный документ на указанный целевой язык. Эта операция использует подключённую модель [AI](../../) для перевода контента.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Документ для перевода. |
| targetLanguage | Aspose::Words::AI::Language | Язык, на который будет переведен документ. |

### ReturnValue

Новый объект [Document](../../../aspose.words/document/), содержащий переведённый документ.

## См. также

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
