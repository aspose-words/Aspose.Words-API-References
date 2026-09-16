---
title: "Aspose::Words::Loading::IResourceLoadingCallback 接口"
linktitle: "IResourceLoadingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::IResourceLoadingCallback 接口。如果您想在使用 C++ 的 DocumentBuilder 导入文档并插入图像时控制 Aspose.Words 加载外部资源的方式，请实现此接口。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.loading/iresourceloadingcallback/
---
## IResourceLoadingCallback interface


如果您想在使用 [DocumentBuilder](../../aspose.words/documentbuilder/) 导入文档并插入图像时控制 Aspose.Words 加载外部资源的方式，请实现此接口。

```cpp
class IResourceLoadingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [ResourceLoading](./resourceloading/)(System::SharedPtr\<Aspose::Words::Loading::ResourceLoadingArgs\>) | 当 Aspose.Words 加载任何外部资源时调用。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
