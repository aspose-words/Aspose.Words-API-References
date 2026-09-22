---
title: "منشئ Aspose::Words::AI::GoogleAiModel::GoogleAiModel"
linktitle: "GoogleAiModel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::AI::GoogleAiModel::GoogleAiModel. يقوم بإنشاء نسخة جديدة من الفئة GoogleAiModel في C++."
type: docs
weight: 1500
url: /ar/cpp/aspose.words.ai/googleaimodel/googleaimodel/
---
## GoogleAiModel::GoogleAiModel(const System::String\&) constructor


يقوم بإنشاء نسخة جديدة من الفئة [GoogleAiModel](../).

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | const System::String\& | اسم النموذج. على سبيل المثال، gemini-2.5-flash. |

## أمثلة



يظهر كيفية استخدام نموذج جوجل [AI](../../).
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## انظر أيضًا

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
## GoogleAiModel::GoogleAiModel(const System::String\&, const System::String\&) constructor


يقوم بإنشاء نسخة جديدة من الفئة [GoogleAiModel](../).

```cpp
Aspose::Words::AI::GoogleAiModel::GoogleAiModel(const System::String &name, const System::String &apiKey)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| name | const System::String\& | اسم النموذج. على سبيل المثال، gemini-2.5-flash. |
| apiKey | const System::String\& | مفتاح API لاستخدام Gemini API. يرجى الرجوع إلى [https://ai.google.dev/gemini-api/docs/api-key](https://ai.google.dev/gemini-api/docs/api-key) للحصول على التفاصيل. |

## أمثلة



يظهر كيفية استخدام نموذج جوجل [AI](../../).
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## انظر أيضًا

* Class [GoogleAiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
