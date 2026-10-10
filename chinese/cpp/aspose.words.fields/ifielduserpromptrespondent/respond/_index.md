---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond 方法"
linktitle: "响应"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond 方法。实现后，返回用户在提示时的响应。您的实现应返回 null，以表示用户未对提示作出响应（即用户在提示窗口中点击了取消按钮），在 C++ 中。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent::Respond method


实现后，返回用户在提示时的响应。您的实现应返回 **null** 以表示用户未对提示作出响应（即用户在提示窗口中按下了取消按钮）。

```cpp
virtual System::String Aspose::Words::Fields::IFieldUserPromptRespondent::Respond(System::String promptText, System::String defaultResponse)=0
```


| 参数 | 类型 | 描述 |
| --- | --- | --- |
| promptText | System::String | 提示文本（即提示窗口的标题）。 |
| defaultResponse | System::String | 默认用户响应（即提示窗口中包含的初始值）。 |

### ReturnValue

用户响应（即提示窗口中确认的值）。

## 另见

* Interface [IFieldUserPromptRespondent](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
