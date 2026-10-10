---
title: "Aspose::Words::Saving::IDocumentSavingCallback 接口"
linktitle: "IDocumentSavingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::IDocumentSavingCallback 接口。如果您希望在 C++ 中保存文档期间调用自定义方法，请实现此接口。"
type: docs
weight: 41000
url: /zh/cpp/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface


如果您希望在保存文档期间调用自定义方法，请实现此接口。

```cpp
class IDocumentSavingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\>) | 此方法用于通知文档保存进度。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
