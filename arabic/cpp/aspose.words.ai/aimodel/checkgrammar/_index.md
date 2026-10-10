---
title: "طريقة Aspose::Words::AI::AiModel::CheckGrammar"
linktitle: "CheckGrammar"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::AI::AiModel::CheckGrammar. يتحقق من قواعد اللغة للمستند المقدم. تستفيد هذه العملية من نموذج AI المتصل للتحقق من قواعد اللغة للمستند في C++."
type: docs
weight: 2500
url: /ar/cpp/aspose.words.ai/aimodel/checkgrammar/
---
## AiModel::CheckGrammar method


يتحقق من قواعد اللغة للمستند المقدم. تستفيد هذه العملية من نموذج [AI](../../) المتصل للتحقق من قواعد اللغة للمستند.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::CheckGrammar(System::SharedPtr<Aspose::Words::Document> sourceDocument, System::SharedPtr<Aspose::Words::AI::CheckGrammarOptions> options=nullptr)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | المستند الذي يتم التحقق من قواعد لغته. |
| خيارات | System::SharedPtr\<Aspose::Words::AI::CheckGrammarOptions\> | إعدادات اختيارية للتحكم في كيفية التحقق من القواعد. |

### ReturnValue

مستند جديد [Document](../../../aspose.words/document/) مع قواعد لغة تم التحقق منها.

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

* Class [Document](../../../aspose.words/document/)
* Class [CheckGrammarOptions](../../checkgrammaroptions/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
