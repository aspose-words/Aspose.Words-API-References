---
title: "Aspose::Words::AI::AnthropicAiModel فئة"
linktitle: "AnthropicAiModel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::AI::AnthropicAiModel فئة. فئة تجريدية تمثل التكامل مع نماذج الذكاء الاصطناعي الخاصة بـ Anthropic داخل Aspose.Words في C++."
type: docs
weight: 1250
url: /ar/cpp/aspose.words.ai/anthropicaimodel/
---
## AnthropicAiModel class


فئة تجريدية تمثل التكامل مع نماذج [AI](../) الخاصة بـ Anthropic داخل [Aspose.Words](../../aspose.words/).

```cpp
class AnthropicAiModel : public Aspose::Words::AI::AiModel
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [AnthropicAiModel](./anthropicaimodel/)() |  |
| virtual [CheckGrammar](../aimodel/checkgrammar/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\>) | يفحص قواعد اللغة للمستند المقدم. تستفيد هذه العملية من نموذج [AI](../) المتصل لفحص قواعد اللغة للمستند. |
| static [Create](../aimodel/create/)(Aspose::Words::AI::AiModelType) | ينشئ مثلاً جديداً من فئة [AiModel](../aimodel/). |
| [get_Timeout](../aimodel/get_timeout/)() const | يحصل أو يضبط عدد المللي ثانية التي يجب الانتظار قبل انتهاء مهلة الطلب إلى نموذج [AI](../). القيمة الافتراضية هي 100,000 مللي ثانية (100 ثانية). |
| [get_Url](./get_url/)() override | يحصل على عنوان URL للنموذج. القيمة الافتراضية هي "https://api.anthropic.com/". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Timeout](../aimodel/set_timeout/)(int32_t) | مُحدد لـ [Aspose::Words::AI::AiModel::get_Timeout](../aimodel/get_timeout/). |
| [set_Url](./set_url/)(System::String) override | يضبط عنوان URL للنموذج. القيمة الافتراضية هي "https://api.anthropic.com/". |
| [Summarize](./summarize/)(System::SharedPtr\<Aspose::Words::Document\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | يولد ملخصًا للمستند المحدد، مع خيارات لضبط طول الملخص. تستفيد هذه العملية من نموذج [AI](../) المتصل لمعالجة المحتوى. |
| [Summarize](./summarize/)(System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>, System::SharedPtr\<Aspose::Words::AI::SummarizeOptions\>) override | يولد ملخصات لمجموعة من المستندات، مع خيارات للتحكم في طول الملخص وإعدادات أخرى. تستخدم هذه الطريقة نموذج [AI](../) المتصل لمعالجة كل مستند في المجموعة. |
| [Translate](./translate/)(System::SharedPtr\<Aspose::Words::Document\>, Aspose::Words::AI::Language) override | يترجم المستند المقدم إلى اللغة الهدف المحددة. تستفيد هذه العملية من نموذج [AI](../) المتصل لترجمة المحتوى. |
| static [Type](./type/)() |  |
| [WithApiKey](../aimodel/withapikey/)(const System::String\&) | يضبط مفتاح API المحدد للنموذج. |
## انظر أيضًا

* Class [AiModel](../aimodel/)
* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
