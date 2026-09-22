---
title: "طريقة Aspose::Words::AI::AiModel::Translate"
linktitle: "ترجمة"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::AI::AiModel::Translate. تقوم بترجمة المستند المقدم إلى اللغة الهدف المحددة. تستفيد هذه العملية من نموذج AI المتصل لترجمة المحتوى في C++."
type: docs
weight: 4667
url: /ar/cpp/aspose.words.ai/aimodel/translate/
---
## AiModel::Translate method


يترجم المستند المقدم إلى اللغة الهدف المحددة. تستفيد هذه العملية من نموذج [AI](../../) المتصل لترجمة المحتوى.

```cpp
virtual System::SharedPtr<Aspose::Words::Document> Aspose::Words::AI::AiModel::Translate(System::SharedPtr<Aspose::Words::Document> sourceDocument, Aspose::Words::AI::Language targetLanguage)=0
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| sourceDocument | System::SharedPtr\<Aspose::Words::Document\> | المستند المراد ترجمته. |
| targetLanguage | Aspose::Words::AI::Language | اللغة التي سيتم ترجمة المستند إليها. |

### ReturnValue

كائن [Document](../../../aspose.words/document/) جديد يحتوي على المستند المترجم.

## أمثلة



يعرض كيفية ترجمة النص باستخدام نماذج جوجل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
// استخدم نماذج اللغة التوليدية من Google.
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::GeminiFlashLatest)->WithApiKey(apiKey);

System::SharedPtr<Aspose::Words::Document> translatedDoc = model->Translate(doc, Aspose::Words::AI::Language::Arabic);
translatedDoc->Save(get_ArtifactsDir() + u"AI.AiTranslate.docx");
```

## انظر أيضًا

* Class [Document](../../../aspose.words/document/)
* Enum [Language](../../language/)
* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
