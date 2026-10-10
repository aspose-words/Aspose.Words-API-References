---
title: "Aspose::Words::Saving::IResourceSavingCallback 接口"
linktitle: "IResourceSavingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::IResourceSavingCallback 接口。如果您想在 C++ 中将文档保存为固定页面 HTML 或 SVG 时控制 Aspose.Words 如何保存外部资源（图像、字体和 css），请实现此接口。"
type: docs
weight: 45000
url: /zh/cpp/aspose.words.saving/iresourcesavingcallback/
---
## IResourceSavingCallback interface


如果您想控制 Aspose.Words 在将文档保存为固定页面 HTML 或 SVG 时如何保存外部资源（图像、字体和 css），请实现此接口。

```cpp
class IResourceSavingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceSaving](./resourcesaving/)(System::SharedPtr\<Aspose::Words::Saving::ResourceSavingArgs\>) | 当 Aspose.Words 将外部资源保存为固定页面 HTML 或 SVG 格式时调用。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
