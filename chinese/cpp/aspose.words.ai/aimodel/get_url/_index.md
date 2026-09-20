---
title: "Aspose::Words::AI::AiModel::get_Url 方法"
linktitle: "get_Url"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::AiModel::get_Url 方法。 获取或设置模型的 URL。 默认值在 C++ 中针对该模型是特定的。"
type: docs
weight: 2834
url: /zh/cpp/aspose.words.ai/aimodel/get_url/
---
## AiModel::get_Url method


获取或设置模型的 URL。默认值针对模型是特定的。

```cpp
virtual System::String Aspose::Words::AI::AiModel::get_Url()=0
```


## 示例



展示如何更改模型的默认 URL。
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// 默认值 "https://api.openai.com/"。
model->set_Url(u"https://my.a.com/");
```

## 另见

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
