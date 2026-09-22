---
title: "Aspose::Words::AI::GoogleAiModel فئة"
linktitle: "GoogleAiModel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::AI::GoogleAiModel فئة. فئة تمثل تكامل نماذج Google AI (Gemini) داخل Aspose.Words بلغة C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.ai/googleaimodel/
---
## GoogleAiModel class


فئة تمثل نماذج Google [AI](../) (Gemini) داخل [Aspose.Words](../../aspose.words/).

```cpp
class GoogleAiModel : public Aspose::Words::AI::AiModel
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | يفحص قواعد اللغة للمستند المقدم. تستفيد هذه العملية من نموذج [AI](../) المتصل لفحص قواعد اللغة للمستند. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | ينشئ مثلاً جديداً من فئة [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | يحصل أو يضبط عدد المللي ثانية التي يجب الانتظار قبل انتهاء مهلة الطلب إلى نموذج [AI](../). القيمة الافتراضية هي 100,000 مللي ثانية (100 ثانية). |
| [get_Url](./get_url/)() override | يحصل على عنوان URL للنموذج. القيمة الافتراضية هي "https://generativelanguage.googleapis.com/v1beta/models/". |
| [GetType](./gettype/)() const override |  |
| [GoogleAiModel](./googleaimodel/)(const System::String\&) | يُنشئ مثيلًا جديدًا من فئة [GoogleAiModel](./). |
| [GoogleAiModel](./googleaimodel/)(const System::String\&, const System::String\&) | يُنشئ مثيلًا جديدًا من فئة [GoogleAiModel](./). |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | مُحدد لـ [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | يضبط عنوان URL للنموذج. القيمة الافتراضية هي "https://generativelanguage.googleapis.com/v1beta/models/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | يلخص كائن [Document](../../aspose.words/document/) المحدد. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | يلخص كائنات [Document](../../aspose.words/document/) المحددة. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | يترجم مستندًا محددًا. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | يضبط مفتاح API المحدد للنموذج. |

## أمثلة



يُظهر كيفية تلخيص النص باستخدام نماذج OpenAI و Google.
```cpp
auto firstDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto secondDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// استخدم نماذج اللغة التوليدية من OpenAI أو Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = (System::ExplicitCast<Aspose::Words::AI::OpenAiModel>(Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey)))->WithOrganization(u"Organization")->WithProject(u"Project");

auto options = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Short);
System::SharedPtr<Aspose::Words::Document> oneDocumentSummary = model->Summarize(firstDoc, options);
oneDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.One.docx");

options->set_SummaryLength(Aspose::Words::AI::SummaryLength::Long);
System::SharedPtr<Aspose::Words::Document> multiDocumentSummary = model->Summarize(System::MakeArray<System::SharedPtr<Aspose::Words::Document>>({firstDoc, secondDoc}), options);
multiDocumentSummary->Save(get_ArtifactsDir() + u"AI.AiSummarize.Multi.docx");
```


يعرض كيفية استخدام نموذج [AI](../) من جوجل.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
auto model = System::MakeObject<Aspose::Words::AI::GoogleAiModel>(u"gemini-flash-latest", apiKey);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");
auto summarizeOptions = System::MakeObject<Aspose::Words::AI::SummarizeOptions>();
summarizeOptions->set_SummaryLength(Aspose::Words::AI::SummaryLength::VeryShort);
System::SharedPtr<Aspose::Words::Document> summary = model->Summarize(doc, summarizeOptions);
```

## انظر أيضًا

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
