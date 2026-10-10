---
title: "Aspose::Words::AI::AiModel::get_Timeout 方法"
linktitle: "get_Timeout"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::AI::AiModel::get_Timeout 方法。 获取或设置在请求 AI 模型超时前等待的毫秒数。 默认值在 C++ 中为 100,000 毫秒（100 秒）。"
type: docs
weight: 2667
url: /zh/cpp/aspose.words.ai/aimodel/get_timeout/
---
## AiModel::get_Timeout method


获取或设置在请求 [AI](../../) 模型超时前等待的毫秒数。 默认值为 100,000 毫秒（100 秒）。

```cpp
int32_t Aspose::Words::AI::AiModel::get_Timeout() const
```


## 示例



展示如何更改模型的默认超时。
```cpp
System::String apiKey = System::Environment::GetEnvironmentVariable(u"API_KEY");
System::SharedPtr<Aspose::Words::AI::AiModel> model = Aspose::Words::AI::AiModel::Create(Aspose::Words::AI::AiModelType::Gpt4OMini)->WithApiKey(apiKey);
// 默认值 100000ms。
model->set_Timeout(250000);
```

## 另见

* Class [AiModel](../)
* Namespace [Aspose::Words::AI](../../)
* Library [Aspose.Words for C++](../../../)
