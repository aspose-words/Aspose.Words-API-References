---
title: "طريقة Aspose::Words::AI::OpenAiModel::Translate"
linktitle: "ترجمة"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::AI::OpenAiModel::Translate. تُترجم المستند المُقدم إلى اللغة الهدف المحددة. تستفيد هذه العملية من نموذج الذكاء الاصطناعي المتصل لترجمة المحتوى في C++."
type: docs
weight: 3667
url: /ar/cpp/aspose.words.ai/openaimodel/translate/
---
## OpenAiModel::Translate method


يترجم المستند المقدم إلى اللغة الهدف المحددة. تستفيد هذه العملية من نموذج [AI](../../) المتصل لترجمة المحتوى.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | المستند المراد ترجمته. |
| targetLanguage | Aspose::Words::AI::Language | اللغة التي سيتم ترجمة المستند إليها. |

### ReturnValue

كائن [Document](../../../aspose.words/document/) جديد يحتوي على المستند المترجم.

## انظر أيضًا

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
