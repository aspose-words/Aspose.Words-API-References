---
title: "طريقة Aspose::Words::AI::OpenAiModel::Summarize"
linktitle: "Summarize"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::AI::OpenAiModel::Summarize. تُنشئ ملخصات لمجموعة من المستندات، مع خيارات للتحكم في طول الملخص وإعدادات أخرى. تستخدم هذه الطريقة نموذج AI المتصل لمعالجة كل مستند في المجموعة في C++."
type: docs
weight: 3334
url: /ar/cpp/aspose.words.ai/openaimodel/summarize/
---
## OpenAiModel::Summarize(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


ينشئ ملخصات لمصفوفة من المستندات، مع خيارات للتحكم في طول الملخص وإعدادات أخرى. تستخدم هذه الطريقة النموذج المتصل [AI](../../) لمعالجة كل مستند في المصفوفة.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Summarize(System::ArrayPtr<System::SharedPtr<Aspose::Words::Document>> sourceDocuments, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
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
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::Summarize(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) method


يولد ملخصًا للمستند المحدد، مع خيارات لضبط طول الملخص. تستفيد هذه العملية من نموذج [AI](../../) المتصل لمعالجة المحتوى.

```cpp
System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::OpenAiModel::Summarize(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::SummarizeOptions> options=nullptr) override
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
* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
