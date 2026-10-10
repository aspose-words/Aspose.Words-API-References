---
title: "Aspose::Words::AI::OpenAiModel فئة"
linktitle: "OpenAiModel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::AI::OpenAiModel فئة. فئة تمثل تكامل نماذج OpenAi داخل Aspose.Words بلغة C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.ai/openaimodel/
---
## OpenAiModel class


فئة تمثل تكامل نماذج OpenAi داخل [Aspose.Words](../../aspose.words/).

```cpp
class OpenAiModel : public Aspose::Words::AI::AiModel
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | يفحص قواعد اللغة للمستند المقدم. تستفيد هذه العملية من نموذج [AI](../) المتصل لفحص قواعد اللغة للمستند. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | ينشئ مثلاً جديداً من فئة [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | يحصل أو يضبط عدد المللي ثانية التي يجب الانتظار قبل انتهاء مهلة الطلب إلى نموذج [AI](../). القيمة الافتراضية هي 100,000 مللي ثانية (100 ثانية). |
| [get_Url](./get_url/)() override | يحصل على عنوان URL للنموذج. القيمة الافتراضية هي "https://api.openai.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OpenAiModel](./openaimodel/)(const System::String\&, const System::String\&) | يُنشئ مثيلًا جديدًا من فئة [OpenAiModel](./). |
| [OpenAiModel](./openaimodel/)(const System::String\&) | يُنشئ مثيلًا جديدًا من فئة [OpenAiModel](./). |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | مُحدد لـ [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | يضبط عنوان URL للنموذج. القيمة الافتراضية هي "https://api.openai.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | يولد ملخصًا للمستند المحدد، مع خيارات لضبط طول الملخص. تستفيد هذه العملية من نموذج [AI](../) المتصل لمعالجة المحتوى. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | يولد ملخصات لمجموعة من المستندات، مع خيارات للتحكم في طول الملخص وإعدادات أخرى. تستخدم هذه الطريقة نموذج [AI](../) المتصل لمعالجة كل مستند في المجموعة. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | يترجم المستند المقدم إلى اللغة الهدف المحددة. تستفيد هذه العملية من نموذج [AI](../) المتصل لترجمة المحتوى. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | يضبط مفتاح API المحدد للنموذج. |
| [WithOrganization](./withorganization/)(const System::String\&) | يضبط منظمة محددة للنموذج. |
| [WithProject](./withproject/)(const System::String\&) | يضبط مشروعًا محددًا للنموذج. |

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

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
