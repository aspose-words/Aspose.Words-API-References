---
title: "Aspose::Words::Saving::ICssSavingCallback 接口"
linktitle: "ICssSavingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ICssSavingCallback 接口。如果您希望在 C++ 中将文档保存为 HTML 时控制 Aspose.Words 如何保存 CSS（层叠样式表），请实现此接口。"
type: docs
weight: 39000
url: /zh/cpp/aspose.words.saving/icsssavingcallback/
---
## ICssSavingCallback interface


如果您希望在将文档保存为 HTML 时控制 Aspose.Words 如何保存 CSS（层叠 [Style](../../aspose.words/style/) Sheet），请实现此接口。

```cpp
class ICssSavingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [CssSaving](./csssaving/)(System::SharedPtr\<Aspose::Words::Saving::CssSavingArgs\>) | 当 Aspose.Words 保存 CSS（层叠 [Style](../../aspose.words/style/) Sheet）时调用。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
