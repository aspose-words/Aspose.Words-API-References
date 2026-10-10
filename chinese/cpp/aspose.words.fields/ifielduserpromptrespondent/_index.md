---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent interface"
linktitle: "IFieldUserPromptRespondent"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent interface. 表示在 C++ 中字段更新期间对用户提示作出响应的对象。"
type: docs
weight: 125000
url: /zh/cpp/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface


表示在字段更新期间对用户提示的响应者。

```cpp
class IFieldUserPromptRespondent : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Respond](./respond/)(System::String, System::String) | 实现后，返回用户在提示时的响应。您的实现应返回 **null** 以表示用户未对提示作出响应（即用户在提示窗口中按下了取消按钮）。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
