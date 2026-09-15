---
title: "منشئ Aspose::Words::AI::OpenAiModel::OpenAiModel"
linktitle: "OpenAiModel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::AI::OpenAiModel::OpenAiModel. يهيئ مثالًا جديدًا من فئة OpenAiModel في C++."
type: docs
weight: 1334
url: /ar/cpp/aspose.words.ai/openaimodel/openaimodel/
---
## OpenAiModel::OpenAiModel(const System::String\&) constructor


يهيئ مثالًا جديدًا من فئة [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | const System::String\& | اسم النموذج. على سبيل المثال، gpt-5.2-chat-latest. |

## انظر أيضًا

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## OpenAiModel::OpenAiModel(const System::String\&, const System::String\&) constructor


يهيئ مثالًا جديدًا من فئة [OpenAiModel](../).

```cpp
Aspose::Words::AI::OpenAiModel::OpenAiModel(const System::String &name, const System::String &apiKey)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | const System::String\& | اسم النموذج. على سبيل المثال، gpt-5.2-chat-latest. |
| apiKey | const System::String\& | مفتاح API لاستخدام OpenAi API. |

## أمثلة



يوضح كيفية إنشاء مثال نموذج OpenAI مباشرةً باستخدام مفتاح API واسم النموذج.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// إنشاء مثال نموذج OpenAI باستخدام المنشئ مع اسم النموذج ومفتاح API.
auto model = System::MakeObject<Aspose::Words::AI::OpenAiModel>(u"gpt-4o-mini", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
// تلخيص المستند باستخدام نموذج OpenAI بطول ملخص قصير.
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);

summary->Save(get_ArtifactsDir() + u"OpenAiModel.OpenAiModelConstructor.docx");
```

## انظر أيضًا

* Class [OpenAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
