---
title: "Aspose::Words::AI::AnthropicAiModel::Translate method"
linktitle: "Перевести"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::AI::AnthropicAiModel::Translate method. Переводит предоставленный документ на указанный целевой язык. Эта операция использует подключённую модель AI для перевода контента в C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.ai/anthropicaimodel/translate/
---
## AnthropicAiModel::Translate method


Переводит предоставленный документ на указанный целевой язык. Эта операция использует подключённую модель [AI](../../) для перевода контента.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AnthropicAiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage) override
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
* Class [AnthropicAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
