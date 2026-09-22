---
title: "طريقة Aspose::Words::AI::AiModel::get_Url"
linktitle: "get_Url"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::AI::AiModel::get_Url. يحصل على عنوان URL للنموذج أو يضبطه. القيمة الافتراضية مخصصة للنموذج في C++."
type: docs
weight: 2834
url: /ar/cpp/aspose.words.ai/aimodel/get_url/
---
## AiModel::get_Url method


يحصل أو يضبط عنوان URL للنموذج. القيمة الافتراضية محددة للنموذج.

```cpp
virtual System::String Aspose::Words::AI::AiModel::get_Url()=0
```


## أمثلة



يظهر كيفية تغيير عنوان URL الافتراضي للنموذج.
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// القيمة الافتراضية "https://api.openai.com/".
model->set_Url(u"https://my.a.com/");
```

## انظر أيضًا

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
