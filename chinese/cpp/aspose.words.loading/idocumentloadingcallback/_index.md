---
title: "Aspose::Words::Loading::IDocumentLoadingCallback 接口"
linktitle: "IDocumentLoadingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Loading::IDocumentLoadingCallback 接口。如果您希望在 C++ 中加载文档时调用自己的自定义方法，请实现此接口。"
type: docs
weight: 10000
url: /zh/cpp/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface


如果您希望在加载文档期间调用自己的自定义方法，请实现此接口。

```cpp
class IDocumentLoadingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\>) | 此方法在通知文档加载进度时被调用。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
