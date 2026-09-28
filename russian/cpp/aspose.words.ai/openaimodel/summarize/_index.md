---
title: "Метод Aspose::Words::AI::OpenAiModel::Summarize"
linktitle: "Summarize"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::AI::OpenAiModel::Summarize. Генерирует резюме для массива документов с возможностью управления длиной резюме и другими параметрами. Этот метод использует подключенную AI‑модель для обработки каждого документа в массиве в C++."
type: docs
weight: 3334
url: /ru/cpp/aspose.words.ai/openaimodel/summarize/
---
## OpenAiModel::Summarize(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Генерирует резюме для массива документов, с параметрами для управления длиной резюме и другими настройками. Этот метод использует подключённую модель [AI](../../) для обработки каждого документа в массиве.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Summarize(System::ArrayPtr<System::SharedPtr<Aspose::Words::Document>> sourceDocuments, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocuments | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\> | Массив документов для резюмирования. |
| параметры | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Необязательные настройки для контроля длины резюме и других параметров |

### ReturnValue

Сокращённая версия содержимого документа.

## См. также

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::Summarize(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


Создаёт резюме указанного документа с возможностью настройки длины резюме. Эта операция использует подключённую модель [AI](../../) для обработки контента.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Summarize(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | Документ для резюмирования. |
| параметры | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | Необязательные настройки для контроля длины резюме и других параметров. |

### ReturnValue

Сокращённая версия содержимого документа.

## См. также

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
