---
title: "Aspose::Words::AI::AnthropicAiModel::Summarize طريقة"
linktitle: "Summarize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::AI::AnthropicAiModel::Summarize طريقة. ينشئ ملخصات لمصفوفة من المستندات، مع خيارات للتحكم في طول الملخص وإعدادات أخرى. تستخدم هذه الطريقة نموذج الذكاء الاصطناعي المتصل لمعالجة كل مستند في المصفوفة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.ai/anthropicaimodel/summarize/
---
## AnthropicAiModel::Summarize(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


ينشئ ملخصات لمصفوفة من المستندات، مع خيارات للتحكم في طول الملخص وإعدادات أخرى. تستخدم هذه الطريقة النموذج المتصل [AI](../../) لمعالجة كل مستند في المصفوفة.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AnthropicAiModel::Summarize(System::ArrayPtr<System::SharedPtr<Aspose::Words::Document>> sourceDocuments, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| sourceDocuments | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\> | مصفوفة من المستندات لتلخيصها. |
| خيارات | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | إعدادات اختيارية للتحكم في طول الملخص ومعلمات أخرى |

### ReturnValue

نسخة ملخصة من محتوى المستند.

## انظر أيضًا

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [AnthropicAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## AnthropicAiModel::Summarize(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


يولد ملخصًا للمستند المحدد، مع خيارات لضبط طول الملخص. تستفيد هذه العملية من نموذج [AI](../../) المتصل لمعالجة المحتوى.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AnthropicAiModel::Summarize(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | المستند المراد تلخيصه. |
| خيارات | System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\> | إعدادات اختيارية للتحكم في طول الملخص ومعلمات أخرى. |

### ReturnValue

نسخة ملخصة من محتوى المستند.

## انظر أيضًا

* Class [Document](../../../aspose.words/document/)
* Class [SummarizeOptions](../../summarizeoptions/)
* Class [AnthropicAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
