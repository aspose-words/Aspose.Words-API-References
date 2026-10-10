---
title: "Aspose::Words::Layout::IPageLayoutCallback 接口"
linktitle: "IPageLayoutCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::IPageLayoutCallback 接口。如果您希望在 C++ 中的页面布局模型构建和渲染期间调用自己的自定义方法，请实现此接口。"
type: docs
weight: 6000
url: /zh/cpp/aspose.words.layout/ipagelayoutcallback/
---
## IPageLayoutCallback interface


如果您希望在页面布局模型的构建和渲染期间调用自定义方法，请实现此接口。

```cpp
class IPageLayoutCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Layout::PageLayoutCallbackArgs\>) | 此方法用于通知布局构建和渲染的进度。 |
| static [Type](./type/)() |  |
## 备注


此接口的主要用途是允许应用程序代码中止构建过程。

可以仅在文档开始时为少数页面构建页面布局模型，然后中止过程并仅渲染已构建的部分。

但请注意，渲染结果可能与如果过程完成时每页的渲染结果不匹配。

此技术可能并非适用于所有文档，或可能完全失败。

## 另见

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
