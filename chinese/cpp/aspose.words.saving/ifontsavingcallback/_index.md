---
title: "Aspose::Words::Saving::IFontSavingCallback 接口"
linktitle: "IFontSavingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::IFontSavingCallback 接口。如果您希望在 C++ 中将文档导出为 HTML 格式时接收通知并控制 Aspose.Words 保存字体的方式，请实现此接口。"
type: docs
weight: 42000
url: /zh/cpp/aspose.words.saving/ifontsavingcallback/
---
## IFontSavingCallback interface


如果您想在将文档导出为 HTML 格式时接收通知并控制 Aspose.Words 如何保存字体，请实现此接口。

```cpp
class IFontSavingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [FontSaving](./fontsaving/)(System::SharedPtr\<Aspose::Words::Saving::FontSavingArgs\>) | 当 Aspose.Words 即将保存字体资源时被调用。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
