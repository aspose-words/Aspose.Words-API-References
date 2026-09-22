---
title: "فئة Aspose::Words::AI::AiModel"
linktitle: "AiModel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::AI::AiModel. فئة مجردة تمثل التكامل مع نماذج AI المختلفة داخل Aspose.Words في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.ai/aimodel/
---
## AiModel class


فئة مجردة تمثل التكامل مع نماذج [AI](../) المختلفة داخل [Aspose.Words](../../aspose.words/).

```cpp
class AiModel : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [CheckGrammar](./checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | يفحص قواعد اللغة للمستند المقدم. تستفيد هذه العملية من نموذج [AI](../) المتصل لفحص قواعد اللغة للمستند. |
| static [Create](./create/)(Aspose::Words::AI::AiModelType) | ينشئ مثيلًا جديدًا من فئة [AiModel](./). |
| [get_Timeout](./get_timeout/)() const | يحصل أو يضبط عدد المللي ثانية التي يجب الانتظار قبل انتهاء مهلة الطلب إلى نموذج [AI](../). القيمة الافتراضية هي 100,000 مللي ثانية (100 ثانية). |
| virtual [get_Url](./get_url/)() | يحصل أو يضبط عنوان URL للنموذج. القيمة الافتراضية محددة للنموذج. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](./set_timeout/)(int32_t) | مُحدد لـ [Aspose::Words::AI::AiModel::get_Timeout](./get_timeout/). |
| virtual [set_Url](./set_url/)(System::String) | مُحدد لـ [Aspose::Words::AI::AiModel::get_Url](./get_url/). |
| virtual [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | يولد ملخصًا للمستند المحدد، مع خيارات لضبط طول الملخص. تستفيد هذه العملية من نموذج [AI](../) المتصل لمعالجة المحتوى. |
| virtual [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) | يولد ملخصات لمجموعة من المستندات، مع خيارات للتحكم في طول الملخص وإعدادات أخرى. تستخدم هذه الطريقة نموذج [AI](../) المتصل لمعالجة كل مستند في المجموعة. |
| virtual [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) | يترجم المستند المقدم إلى اللغة الهدف المحددة. تستفيد هذه العملية من نموذج [AI](../) المتصل لترجمة المحتوى. |
| static [Type](./type/)() |  |
| [WithApiKey](./withapikey/)(const System::String\&) | يضبط مفتاح API المحدد للنموذج. |

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

## انظر أيضًا

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
