---
title: "Aspose::Words::Saving::IDocumentPartSavingCallback 接口"
linktitle: "IDocumentPartSavingCallback"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::IDocumentPartSavingCallback 接口。如果您希望在 C++ 中将文档导出为 Html 或 Epub 格式时接收通知并控制 Aspose.Words 保存文档部分的方式，请实现此接口。"
type: docs
weight: 40000
url: /zh/cpp/aspose.words.saving/idocumentpartsavingcallback/
---
## IDocumentPartSavingCallback interface


如果您希望在将文档导出为 [Html](../../aspose.words/saveformat/) 或 [Epub](../../aspose.words/saveformat/) 格式时接收通知并控制 Aspose.Words 保存文档部分的方式，请实现此接口。

```cpp
class IDocumentPartSavingCallback : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [DocumentPartSaving](./documentpartsaving/)(System::SharedPtr\<Aspose::Words::Saving::DocumentPartSavingArgs\>) | 当 Aspose.Words 即将保存文档部分时调用。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
