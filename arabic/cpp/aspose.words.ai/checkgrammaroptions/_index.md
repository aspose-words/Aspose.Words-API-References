---
title: "Aspose::Words::AI::CheckGrammarOptions فئة"
linktitle: "CheckGrammarOptions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::AI::CheckGrammarOptions فئة. يسمح بتحديد خيارات متعددة أثناء فحص قواعد اللغة لمستند باستخدام الذكاء الاصطناعي في C++."
type: docs
weight: 1500
url: /ar/cpp/aspose.words.ai/checkgrammaroptions/
---
## CheckGrammarOptions class


يسمح بتحديد خيارات متعددة أثناء فحص قواعد اللغة لمستند باستخدام [AI](../).

```cpp
class CheckGrammarOptions : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [CheckGrammarOptions](./checkgrammaroptions/)() |  |
| [get_ImproveStylistics](./get_improvestylistics/)() const | يسمح بتحديد ما إذا كان [AI](../) سيحاول تحسين الأسلوب للنص الذي يتم تدقيقه. القيمة الافتراضية هي **false**. |
| [get_MakeRevisions](./get_makerevisions/)() const | يسمح بتحديد ما إذا كان المستند النهائي أو المعدل سيُعاد مع النص المدقق. القيمة الافتراضية هي **false**. |
| [get_PreserveFormatting](./get_preserveformatting/)() const | يسمح بتحديد ما إذا كان [CheckGrammar()](../aimodel/checkgrammar/) سيحاول الحفاظ على تخطيط وتنسيق المستند الأصلي، أم لا. القيمة الافتراضية هي **true**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ImproveStylistics](./set_improvestylistics/)(bool) | يسمح بتحديد ما إذا كان [AI](../) سيحاول تحسين الأسلوب للنص الذي يتم تدقيقه. القيمة الافتراضية هي **false**. |
| [set_MakeRevisions](./set_makerevisions/)(bool) | يسمح بتحديد ما إذا كان المستند النهائي أو المعدل سيُعاد مع النص المدقق. القيمة الافتراضية هي **false**. |
| [set_PreserveFormatting](./set_preserveformatting/)(bool) | يسمح بتحديد ما إذا كان [CheckGrammar()](../aimodel/checkgrammar/) سيحاول الحفاظ على تخطيط وتنسيق المستند الأصلي، أم لا. القيمة الافتراضية هي **true**. |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية فحص قواعد اللغة لمستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// استخدم نماذج اللغة التوليدية من OpenAI.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);

auto grammarOptions = System::MakeObject<Aspose::Words::AI::CheckGrammarOptions>();
grammarOptions->set_ImproveStylistics(true);

System::SharedPtr<Aspose::Words::Document> proofedDoc = model->CheckGrammar(doc, grammarOptions);
proofedDoc->Save(get_ArtifactsDir() + u"AI.AiGrammar.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words::AI](../)
* Library [Aspose.Words for C++](../../)
