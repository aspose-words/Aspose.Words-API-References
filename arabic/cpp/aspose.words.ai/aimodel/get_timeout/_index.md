---
title: "طريقة Aspose::Words::AI::AiModel::get_Timeout"
linktitle: "get_Timeout"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::AI::AiModel::get_Timeout. تحصل أو تعين عدد الملليثواني التي يجب الانتظار قبل انتهاء مهلة الطلب إلى نموذج AI. القيمة الافتراضية هي 100,000 ملليثانية (100 ثانية) في C++."
type: docs
weight: 2667
url: /ar/cpp/aspose.words.ai/aimodel/get_timeout/
---
## AiModel::get_Timeout method


تحصل أو تعين عدد الملليثواني التي يجب الانتظار قبل انتهاء مهلة الطلب إلى نموذج [AI](../../). القيمة الافتراضية هي 100,000 ملليثانية (100 ثانية).

```cpp
int32_t Aspose::Words::AI::AiModel::get_Timeout() const
```


## أمثلة



يوضح كيفية تغيير مهلة النموذج الافتراضية.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// القيمة الافتراضية 100000 ملليثانية.
model->set_Timeout(250000);
```

## انظر أيضًا

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
