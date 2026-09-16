---
title: "Aspose::Words::Layout::PageLayoutCallbackArgs class"
linktitle: "PageLayoutCallbackArgs"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Layout::PageLayoutCallbackArgs 类。传递给 Notify() 的参数。了解更多，请访问 C++ 文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.layout/pagelayoutcallbackargs/
---
## PageLayoutCallbackArgs class


传递给 [Notify()](../ipagelayoutcallback/notify/) 的参数。了解更多，请访问 [Converting to Fixed-page Format](https://docs.aspose.com/words/cpp/converting-to-fixed-page-format/) 文档文章。

```cpp
class PageLayoutCallbackArgs : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Document](./get_document/)() const | 获取文档。 |
| [get_Event](./get_event/)() const | 获取事件。 |
| [get_PageIndex](./get_pageindex/)() | 获取此事件关联的文档中页面的 0 基索引。如果没有关联页面，或页面在重新流动期间被移除，则返回负值。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
