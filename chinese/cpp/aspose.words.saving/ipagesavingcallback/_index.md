---
title: "Aspose::Words::Saving::IPageSavingCallback 接口"
linktitle: "IPageSavingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::IPageSavingCallback 接口。如果您想在 C++ 中将文档保存为固定页面格式时控制 Aspose.Words 如何保存单独的页面，请实现此接口。"
type: docs
weight: 44000
url: /zh/cpp/aspose.words.saving/ipagesavingcallback/
---
## IPageSavingCallback interface


如果您想控制 Aspose.Words 在将文档保存为固定页面格式时如何保存单独页面，请实现此接口。

```cpp
class IPageSavingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [PageSaving](./pagesaving/)(System::SharedPtr\<Aspose::Words::Saving::PageSavingArgs\>) | 当 Aspose.Words 将单独的页面保存为固定页面格式时调用。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
