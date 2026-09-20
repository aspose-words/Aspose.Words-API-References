---
title: "Aspose::Words::IDocumentMergerPlugin interface"
linktitle: "IDocumentMergerPlugin"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::IDocumentMergerPlugin 接口。定义一个用于外部合并插件的接口，可在 C++ 中合并 PDF 文档。"
type: docs
weight: 76500
url: /zh/cpp/aspose.words/idocumentmergerplugin/
---
## IDocumentMergerPlugin interface


定义可合并 PDF 文档的外部合并插件的接口。

```cpp
class IDocumentMergerPlugin : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Merge](./merge/)(System::SharedPtr\<System::IO::Stream\>, System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>, System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>) | 使用指定的输入和输出流将给定的输入 PDF 文档合并为单个输出 PDF 文档。 |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
